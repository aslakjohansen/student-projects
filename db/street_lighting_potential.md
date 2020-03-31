# Smart Street Light Potential

**Tags:** open data, cost benefit, simulation, operational regimes

## Introduction

Lots of energy goes into street lighting. Yet most street lights operate on a timer (or something resembling it). One can easily imagine that we can improve service (by introducing dimmable lights) and/or consumption (by introducing sensors to detect use), but it is not clear how this would affect cost, complexity, and security of the roads. In this project, we try to estimate and bound the cost perspective.

Open datasets are available that details the road layout of Denmark and (to a lesser degree) how much these roads are used. These open datasets include:
- [Open Street Maps](https://wiki.openstreetmap.org/wiki/Downloading_data)
- [Danish Open Data Portal](https://portal.opendata.dk)

Street lights are placed at certain intervals in order to be able to provide a reasonable amount of light at all streets.

The assumption in this project is that any part of a street within 20 meters of a pedestrian, 50 meters of a cyclist or 100 meters of a car needs to be lit.

## Problem

In this project we seek to answer the following questions:
1. How much energy could theoretically be saved?
2. Which kind of maintenance price is necessary to break even?
3. Would it make sense for a subset of the streets (e.g., highways or pedestrian streets, bike trails, city streets)?

We would like to figure out which combinations of the following hardware make sense when:
- Lamps (always on, on/off controllable, brightness controllable)
- Light sensors (have them or not)
- Arbitrary sensor for detecting whether the road is in use (have them or no).

## Approach

Based on open datasets, descriptions of currently available lighting products, sensible assumptions, and extrapolations, a parameterized model of the consumption of street lights should be constructed.

The process:
1. For each stretch of road, estimate the number of streetlights and the usage pattern.
2. Simulate alternative operational regimes (always on, on/off using a schedule, dynamically based on setpoint, dynamically based on usage, etc.).

## Related Work

