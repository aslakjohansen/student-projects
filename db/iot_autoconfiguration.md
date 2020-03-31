# IoT Autoconfiguration

**Tags:** iot, zeroconf, ontology, brick

## Introduction

One of the key costs of deploying a device (e.g., a sensor) in a building is the configuration. The configuration process involves:
1. Assigning some identifier to the device on whichever bus it was connected to.
2. Defining the device in the building management system (BMS)
3. Configuring the BMS logic to use it
With the introduction of IoT and a metadata schema like Brick we can propose an alternative process.

Brick is an RDF-based ontology for describing the equipment and relationships within a building. 

A Brick server is used to store a model of a building based on the Brick schema and offers services for updating and querying the model.

## Problem

In order to support automatically configurable new devices, we want to investigate:
1. What information needs to be stored on the device?
2. How hardcoded does this need to be?
3. How will the device know about the Brick server?
4. How much of the registration task can be automated?
5. What should the registration interface look like?
6. Is a Brick extension necessary to to support this use-case, and if so what should it look like?

## Approach

Zeroconf should be used for locating an appropriate Brick server.

A dummy brick server need to be constructed.

## Related Work

- [Zeroconf](https://en.wikipedia.org/wiki/Zero-configuration_networking)
- [Brick](https://brickschema.org)

