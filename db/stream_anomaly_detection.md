# Platform for Anomaly Detection in Data Streams

**Tags:** web, anomaly detection, streaming data, platform, ontology, brick, clustering

## Introduction

At the Center for Energy Informatics we are collecting data from a nontrivial number of sensors. These cover temperature, humidity, co2, light levels, power consumption, valve positions amongst others. Each sensor produces a stream of timeseries data and is associated with some metadata.

We have observed several kind of sensor-level faults, including
- Mislabeled sensors
- Sensors which reading quality degrade over time
- Sensors which stop reporting

While some of these problems can easily be monitored by logic given certain parameters, others need a human in the loop.

The relationships between these streams and the building they monitor is described in a [Brick](https://brickschema.org) model. 

## Problem

In this project we seek to build a platform for monitoring these streams and process them in such a way that anomalies will stand out the a human through summary information on a dashboard. It should be possible to define assertions through a set of queries (against a Brick model) and some logic.

## Approach

The platforms should cluster streams of each type according to similarity and order them to minimize differences of successive streams. Then a live heatmap should be displayed for each stream type, with one row of pixels per stream and the columns used to represent time. As ned values are received this window should scroll on the time axis. Streams which are behind in reporting should be indicated with red.

Each configured assertion then effectively acts as a new sensor type, and each match of the queries ends up being mapped to a new stream of this type.

## Related Work

- [Distil](http://sdb.cs.berkeley.edu/sdb/distil.php)

