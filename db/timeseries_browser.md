# Timeseries Browser

**Tags:** web, ui, ontology brick, sparql, parsing, pubsub

## Introduction

A typical commercial building produces a large number of data streams. The OU44 teaching building (the one housing U180) produces tens of thousands streams. These streams come from a number of different systems and are rarely well organized when exposed. To understand these streams we have historically annotated each stream with a key-value store for metadata. We have then defined tree structures through these keys and used an online tool to choose and plot a subset of these streams from the tree structures. This tool had several restriction. The main issue was a user experience when choosing a subset of the streams.

In the meantime it has turned out that a key-value store is not descriptive enough for metadata, and we have are now in the process of transitioning to the [brick](https://brickschema.org) ontology for describing buildings. Brick is RDF-based and thus provides a much stronger metadata platform. We would like to see how a plotter can make use of this to select streams for plotting.

## Problem

How should the stream selector for a new plotter look?

It should allows us to browse the available streams in a convenient way.

## Approach

The approach should be to use a SparQL query to select the data streams.

One could define a set of common patterns and have the system suggest “snapping” the query to these.

## Related Work

- [UPMU Plotter](https://github.com/SoftwareDefinedBuildings/upmu-plotter)

