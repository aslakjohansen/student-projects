# Brick Maps

**Tags:** web, ui, ontology, brick, maps, shortest path, factor choosing, gis

## Introduction

Google maps is a service for viewing a window of the globe, for getting summary information on a specific part by dropping a pin, and for guiding a user from their current location to specific part. Surely, google maps does other things. But they are of less relevant to this project.

Brick is an RDF-based metadata schema for describing buildings. The OU44 teaching building at SDU Campus Odense has been fairly well described:
- It can run the [floorviz](https://dl.acm.org/citation.cfm?id=3281014) application. This involves mapping individual rooms to paths in per-floor SVG files.
- We have a list of room connectivity. That is, which rooms are connected to which room using doors, elevators or stairs.
- We have the area and type of every room.
- We have every lamp in every room and their individual wattage.

## Problem

In this project we seek to construct the Brick Maps application, which extends Brick and FloorViz to support the key functionalities of google maps. This includes:
1. Find the most convenient route from one position in the building (e.g., the current) to another.
2. Display key information per room.

## Approach

I imagine a system consisting of
- A web-based frontend similar to that of [FloorViz](https://github.com/aslakjohansen/floorviz)
- Some backend wrapping a brick model (does the shortest path work)
- The brick model having references to some external sources (like the SVG files and paths)

And then have a discussion around how the design should change when we allow changes to the Brick model.

## Related Work

