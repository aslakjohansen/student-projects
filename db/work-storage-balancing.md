# Work-Storage Balancing through Caching

**Tags:** caching, storage, processing, cloud

## Introduction

In data processing there is a dichotomy between original data and derived data. Original data is the raw, unprocessed data, straight from the source. This data then gets processed, enriched, combined and split. The result is derived data.

Original data should be stored. Derived data, on the other hand, can be recreated. Accordingly, storing the data is a matter of performance. The further down the memory hierarchy the data is pushed the higher the latency penalty of accessing it. And if the data is not even stored, then we get the penalty of recreating it. That penalty is dependent on the latency of the data that it was constructed from and the time needed to construct it. Notice that this is a recursive definition, that is eventually rooted in original data.

If large sets of data is being processed then large sets of data are (likely) derived. This is unlikely to stay in the upper levels of the memory hierarchy. Given large enough datasets, some will eventually have to find its way to disk. As disk consumption grows, so does the cost of owning those data. Without knowing the value of individual pieces of data that is a tough job to clean up manually.

Perhaps we could keep track of the time it takes to produce each piece of data, their relationships, and the cost of keeping it stored? Based on that, we could do a cost-risk analysis of the price of hitting certain levels of latency. This would provide a data management knob that could be used to reason about cloud resource consumption.

## Problem

What would the tooling necessary to facilitate the automatic collection of these metrics, and automatically delete data when deemed worthwhile and automatically recreate the data on demand look like?

## Approach

## Related Work

