# Floorplan Generator

**Tags:** image recognition, vectorization

## Introduction

Often buildings don't come with a digital floorplan, and when they do they are rarely in a format that is ready for machine consumption. However, usually we can get a noisy bitmapped floorplan (e.g., from scanning an old drawing or printout). This project aims to transform that into something usable (e.g. an SVG file with a path for each room and a JSON file mapping room names to IDs within this file).

## Problem

How can we transformed a scanned (i.e., bitmapped and noisy) floorplan to vector graphics.

Points will be awarded for automatically:
- Detection of rooms, and defining them as paths in a 2d coordinate system.
- Associating rooms with room names.
- Associating rooms with floor names/numbers.
- Detecting other devices/equipment that are present on the floorplans.
- Associating these devices/equipment with rooms and/or other devices/equipment.

Basically we want to extract as much as possible as automatically as possible.

## Approach

## Related Work

- [FloorViz - a bricked dashboard: demo abstract](https://dl.acm.org/doi/10.1145/3276774.3281014)
- [Raster-to-Vector: Revisiting Floorplan Transformation](https://ieeexplore.ieee.org/document/8237503)

