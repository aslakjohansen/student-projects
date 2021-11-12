# Modeling Zones in an Ontology

**Tags:** ontology, brick, zones, modeling, logic

## Introduction

At the Center for Energy Informatics we are collecting data from a large number of devices (e.g., temperature) and controlling quite a few others (e.g., light levels in rooms). All related to buildings. As an "index" for what is where in a building we use [Brick](https://brickschema.org) models. Brick is an RDF-based ontology which may be queried using a language like SparQL.

With the introduction of more zone types the lack of a well integrated zone concept in Brick becomes more evident. Currently, Brick has HVAC_Zone and Lighting_Zone. These types only resembles each other in name (including their common decomposition to the Zone tag). They are associated to spatial locations in different ways. That makes it decidedly harder to deduce intersection or union operations.

We are currently considering adding occupancy zones, modeling zones and KNX zones. Additionally, we are faced with the issue of having multiple active and relevant room naming conventions for a single building with no trivial mapping. The solution to this problem is likely to interact with a zone concept.

## Problem

Come up with a generic zone concept. The key issues are:
1. What is the relationship between a room and a zone?
2. What to use as the set unit?
3. How to allow set operations?

## Approach

There are three options …

### 1: Service Wrapping a Polygon Database

A zone is mapped to a zone type and a polygon. The polygons (and perhaps the types) are stored in a polygon database (GIS?). When queries are performed the set operations are essentially translated into polygon operations.

For this to make sense, any physical construct within the brick model should be mapped to a zone or point.

### 2: Anchoring Brick Zones in a Hierarchy of Locations

By merging hasLocation and isPartOf a clear hierarchy (or rather acyclic graph) of the spatial nesting of a building can be defined. Any entity in this graph can be decomposed to a set of entities of the same or smaller size.

This is the same mapping making up the defining characteristic of a zone, meaning that any such entity can represent a zone. The spatial granularity is then inherited from the remaining Brick ontology.

It is not clear how to differentiate between three lighting zones at different distances from windows. Solutions includes adding properties and implementing a linked list anchored in a window entity.

### 3: Software-Defined Zones

Implement a server which maintains a real-time model of zones, defined through software. This server has a publish-subscribe interface to allow clients to be notified of changes in the result set of their SparQL queries.

## Open Problem

How can this be done while respecting the access rights?

**Note:** This may generalize to all of Brick.

## Related Work

