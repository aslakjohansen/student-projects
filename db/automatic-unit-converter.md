# Automatic Unit Converter

**Tags:** symbolic manipulation, automation, in-flight data conversion, rdf, graph processing

## Introduction

Building instrumentation produce data streams with values following a wide variety of units. The applications we want to run on these buildings often have a need for values in other units. It is not practical to hardcode lookup-tables for converting any unit to any other unit, and application developers will insist that this is somebody elses problem. In this project we seek to produce an automatic consversion system that can make this a nonissue.

## Problem

Imagine a graph with units, prefixes and modalities as nodes, and functions as edges. That graph could live as an RDF-based information model or in a true graph database.

Imagine another model (e.g., Brick) that describes some domain and the timeseries that are being produces from instrumentation of that domain. Here every timeseries is associated with a unit.

In this project we are going to build a system that given a datastream and a combination of unit and prefix will convert that datastream in-flight. How to do so will be looked up in the first model.

Questions to answer:
- How littel overhead can you get away with?
- How would a system like this embed in a larger system rooted in an RDF-based information model?

## Approach

In short:
1. Look up the shortest path between the datastream (unit, prefix) combo and the requested (unit,prefix) combo.
2. Combine all these formula (from the edges) to one big expression.
3. Simplify the expression.
4. Convert to executable form.
5. Subscribe to data.
6. Convert and forward on reception.

## Related Work

- [SymPy](https://www.sympy.org/en/index.html)
- [Brick](https://brickschema.org)

