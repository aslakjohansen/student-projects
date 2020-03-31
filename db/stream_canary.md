# Stream Canary: Fault Detection Through Inter-Stream Assertions

**Tags:** stream processing, fault detection, signal processing, pattern matching, ontologies

## Introduction

Buildings produce many streams. Some of these are expected to exhibit dependent behaviour. As an example, if a PIR sensor is used to control the light in a room, we can assert certain things about the relationship between the signal from that PIR sensor and the signal from a light sensor in the same room (e.g., the light level drops by 30-40% no more than 120s after the pir sensor signal goes low). This particular assertion will fail the moment a light bulb on the room fails.

## Problem

In this project, we seek to build a system that continuously checks such assertions and allows a user to define such assertions in a scalable way.

## Approach

We will assume the existence of a Brick metadata model for the building.

An assertion is the combination of a SparQL query (to be evaluated against the Brick model) and a definition of the expected behavior. Each application site (match of query against model) is considered. Stream IDs are pulled from the model and subscribed to for streaming data.

Evaluation will be done by replaying historical data.

## Related Work

- [Golang](Golang https://golang.org)
- [Brick](https://portal.findresearcher.sdu.dk/en/publications/brick-metadata-schema-for-portable-smart-building-applications)
- [SparQL](https://en.wikipedia.org/wiki/SPARQL)

