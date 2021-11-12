# Modeling of On-Demand Virtual Sensors

**Tags:** virtual sensor, ontologies, virtual representation, digital twin, brick, query resolution 

## Introduction

We can use models (e.g., ones based on ontologies) to describe both physical and service characteristics of cyber-physical systems. For buildings one choise would be [Brick](https://brickschema.org). However, this ontology (and the equivalents for other domains) only describe physical hardware. This allows us to associate a room with a specific temperature sensor. However, deploying sensors can be costly, and many modalities can be simulated using *virtual sensors*. A virtual sensor is a piece of logic that -- given a configuration of specific inputs -- can produce an output that is reasonably close to what a physical sensor would.

As an example, given the ventilation rate of a room an estimation of the number of occupants can be produced. This is clearly not as precise as a camera-based solution, but for many rooms it comes (theoretically) free of cost.

Ideally, the model of the physical characteristics should be combined with a suite of virtual sensor definitions. These definitions should cover context, requirements, output and how to instantiate it. A query against the system should favor physical sensors, but -- lacking such -- fall back on a strategy of finding a combination of virtual sensor configurations that together can fulfill that role. These should be dynamically be spun up on demand in such a way that the client issuing the query cannot tell the difference simply by looking at the data. Sometimes the client is going to want a confidence qualification of these data (so that they can decide for themselves whether the signal is trustworthy enough for their use case), and that should be offered as well.

## Problem

How should we represent virtual sensors in a Brick model?

In particular, this representation should allow for:
1. Seamless querying across physical and virtual sensors.
2. On-demand instantiation of virtual sensors.

## Approach

## Related Work

- [Brick](https://brickschema.org)
- RDF, RDFS, OWL, SparQL

