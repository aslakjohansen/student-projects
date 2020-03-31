# Distributed RDF Store

**Tags:** distributed systems, dbms, ontology, brick, iot, resource constrained devices, query evaluation

## Introduction

At the Center for Energy Informatics we are collecting data from a large number of devices (e.g., temperature) and controlling quite a few others (e.g., light levels in rooms). All related to buildings. As an "index" for what is where in a building we use [Brick](https://brickschema.org) models. Brick is an RDF-based ontology which may be queried using a language like SparQL.

In order to introduce a new device to the system certain mappings need to be introduced. Conversely, whenever a device is moved this should be reflected in the system.

In this project we seek to explore a setup where the device itself keeps the information it is born with (e.g., which kind of data stream it consumes/produces) and notifies an RDF database housing the Brick model of its existence. That RDF database will then be updated to contain the minimal references needed to name the new device.

Driver software -- tasked with bridging such devices with the overall infrastructure -- will then contact these devices directly and populate the main Brick model.

## Problem

How to maintain the mappings to devices as they are introduced and moved around?

## Approach

Something along the lines of:
1. Each device should hold a "small" RDF-based model.
2. Drivers will query this model and maintain streaming connections to them.
3. Queries against the main model will result in simpler queries against device models (e.g., a subset of SparQL).

## Related Work

