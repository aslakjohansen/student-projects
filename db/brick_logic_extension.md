# Brick Extension Modeling Logic

**Tags:** ontology, brick, logic, modeling, redundancy, graceful degradation

## Introduction

At the Center for Energy Informatics we work with software-defined buildings. We collect data from the buildings, store it to preserve history, process it, visualize it, make control decisions based on it and carry out those control decisions. Each of these are handled by one or more processes. Those are, pieces of code which are executed within some context and generates some outputs based on some inputs. One such piece of code interfaces with an external system to retrieve data on energy consumption.

In order for all this software to agree on which data represents what and goes where we are modeling our buildings using the [Brick](https://brickschema.org) ontology. This ontology is RDF-based and may be queried using SparQL.

We have a need to ...
- trace outages to specific pieces of logic, and to determine which datastreams (and through these applications) depends on a certain piece of code. This needs to be able to deal with redundancy and graceful degradation.
- understand the context well enough to reason about the network topology and automatically restart processes determined to be failing or install new ones.

## Problem

How can we meet these requirements on the modeling plane?

**Note:** This does not include implementing these features in software, but rather implementing support for them in the model.

## Approach

This should be accomplished through an RDF schema which integrates with Brick.

## Related Work

