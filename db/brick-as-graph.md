# Brick as a Graph

**Tags:** metadata, ontology, rdf, graph, automation

## Introduction

[Brick](https://brickschema.org) is a schema for describing the aspects of a building that are relevant to applications running on the building during the operational stage of its lifecycle. It is an RDF-based ontology, and the models that follow this schema are thus stored as triples.

These applications include dashboards, control of HVAC (da: ventilation) systems, control of lighting systems, heating systems, assett location systems, room bookings systems, energy performance calculations, digital assistant integrations, and the list goes on. They are informed through queries against a model that follows such a schema.

The triples of RDF is one way of modeling this. Graphs is another.

## Problem

What would it take to "port" the Brick schema, a model following it, and an application to a graph? What would the benefits be, and what are the disadvantages? To which degree can this porting process be done automatically, so that updates to any of the inputs (Brick schema, building model, application query)?

## Approach

Perhaps use [neo4j](https://neo4j.com)?

## Related Work

