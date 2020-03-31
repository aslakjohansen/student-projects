# Digester

**Tags:** systems, on-demand processing, publish subscribe, dag, non-destructive, stream processing, concurrency, garbage collection, optimization

## Introduction

At the Center for Energy Informatics we are collecting data from tens of thousands of streams. These data ends up in an archiver through which applications can subscribe to incoming data or request historical data. We are modeling our buildings (and how those data streams relates to them) using the [Brick](https://brickschema.org) ontology. This ontology is RDF-based and may be queried using SparQL.

Although these applications have specific preprocessing needs they generally can’t be bothered to implement the logic for this. Instead we would like to construct a service through which the applications can subscribe to “digested” data.

The processing needs include:
- Resampling
  - **Up** Interpolation
  - **Down** Decimation
- Processing
  - **Arithmetic Operations** on streams and constants
  - **Outlier Removal** for cleaning up
  - **Quality Indication** so that clients will know to which degree the signal is trustworthy
- Multistream
  - **Merging** of multiple streams
  - **Splitting** splitting of streams encoding multiple values

## Problem

How can we provide a service that can meet the wide range of processing requirements from such applications?

## Approach

Graph processing (nondestructive DAG) where each node has named inputs and outputs.

- Special nodes:
  - **Source** Essentially a query yielding a (potentially expanding) set of streams
  - **Sink** Any value arriving at a sink gets pushed to all subscribing clients using their preferred protocol.
- Generic nodes:
  - has i named inputs
  - has o named outputs
  - **Undecided:** Are inputs and outputs typed?
- Edges:
  - is simply an indirection

The graph should evolve as clients request processed data and loses interest in it. Nodes should be reused across clients.

## Related Work

- [Distil](http://sdb.cs.berkeley.edu/sdb/distil.php)

