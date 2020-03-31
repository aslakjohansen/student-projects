# Timeseries Archiver

**Tags:** streaming data, acid, distributed systems, timeseries data, concurrency, data structures

## Introduction

At the center for energy informatics we collect and store data from a significant number of streams from equipment in buildings. Each such stream represents a timeseries of values and metadata. That is, a mapping from time to a value (boolean, integral or float) and a key-value store.

Our current archiver setup is becoming problematic to maintain or replicate. We have considered moving to BtrDB, but it requires a cluster to install cleanly. BtrDB is a timeseries database which employs a specialized B+ tree on the datums to cache summary statistics at different temporal granularities. This allows for extremely fast retrieval of summary statistics (to a degree that allows for live zooming) as well as fast inserts.

## Problem

BtrDB scales to tens of millions of writes per second for a single instance. This is not really necessary for us, and we dislike the hardware requirements. So, how much performance would we have to give up if we implement a new tree-based archiver to run on a Raspberry Pi (or a laptop)?

## Approach

Suggested steps:
1. Implement a simple timeseries database (this will act as a baseline)
2. Verify correctness experimentally
3. Design and run benchmark
4. Update database to include tree structure
5. Verify correctness experimentally
6. Extend benchmark to cover tree structure and run it

## Related Work

- BtrDB
  - [Homepage](http://btrdb.io)
  - [Demo](https://www.youtube.com/watch?v=jgA-viRr8go)
- InfluxDB
  - [API](https://docs.influxdata.com/influxdb/v1.7/tools/api/)
  - [Getting started with influxDB (with Golang example)](https://medium.com/spankie/getting-started-with-influxdb-with-golang-example-10990c5efee7)

