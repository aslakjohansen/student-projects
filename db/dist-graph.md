# Distributed Property Graph Database Management System

**Tags:** distibuted systems, dbms, graph, property graph, query evaluation, domain specific language

## Introduction

The property graph is an attractive way of modelling data. Neo4j popularized it and has build abusiness up around it. They provide ACID compliance, hosting options, distribution, and partial open sourcing of the codebase.

Their query language (Cypher) has been standardized as OpenCypher and adopted by multiple players in the industry. The grammar of OpenCypher is publicly available, and the data model is actually quite simple.

## Direction 1: Rely on Existing DMBS

### Problem

What would it take to build a DMBS frontend, that can receive a OpenCypher query, parse it, and distribute the resolution to a set of property graph DBMS?

### Approach

The approach would likely include:
- Focus on a relevant subset of the OpenCypher functionalities.
- Accept that ACID compliance is not ensured.

## Direction 2: Build Own DBMS

### Problem

What would it take to build a generic (distributed) DBMS that is OpenCypher compliant?

### Approach

The approach would likely include:
- Focus on a relevant subset of the OpenCypher functionalities.
- Accept that ACID compliance is not ensured.
- Try to generalize so that multiple domains can be served by framework (e.g., if the `PropertyGraphNode` interface is implemented then the object can be queried).

## Related Work

- [Cypher: An Evolving Query Language for Property Graphs](https://dl.acm.org/doi/10.1145/3183713.3190657)
- [Neo4j](https://neo4j.com)
- [OpenCypher](https://opencypher.org)
- [Neo4j Open Source](https://neo4j.com/open-source-project/)

