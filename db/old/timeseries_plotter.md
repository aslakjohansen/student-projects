# Next Generation Time-Series Plotter

**Tags:** web, data science, svg, visualization

## Introduction

The current plotter used at the Center for Energy Informatics is becoming an annoyance, and the time is ripe for a replacement.

The center for energy informatics collects timeseries data from a variety of sources. As of writing 10s of thousands of streams are being collected from 3 buildings, but both these numbers are growing.

With that amount of streams it is necessary to name and annotate these streams with metadata automatically, and there are often not a whole lot of relevant information to base that name of. Furthermore, these streams come from different subsystems of the buildings and they expose different kinds and levels of metadata.

Interpolation can be tricky as the semantics of a measurement varies with the collection methodology. Some phenomena are sampled at regular intervals. They are easy to deal with. Others are recorded when a measured value differs more than some amount. This introduces the concept of a confidence interval.

## Problem

How can a web-based plotter be constructed which can plot a set of streams in a way which is both illustrative, true to the underlying data, nameable through a permalink and exportable to PDF. This involves visualizing the level of trust (e.g., the confidence interval) in the data.

Since the plotter is to be used in various different applications it should not depend on a particular framework.

## Approach

Create a reusable javascript “component” which combines an SVG object with the needed logic.

## Related Work

- [Mr Plotter](https://github.com/BTrDB/mr-plotter)
- [UPMU Plotter](https://github.com/SoftwareDefinedBuildings/upmu-plotter)

