# Continuous Data Lineage

**Tags:** data lineage, continuous integration, continuous delivery

## Introduction

The lineage of a piece of data is the sequence of transformations that lead from some data source to that piece of data. Those transformations are to result of some pipeline (or DAG, or graph) of operations. Documenting the lineage is key to understanding what derivative data represents, and what they don't represent.

Documenting the lineage of some data produced by a static process is one problem, with several possible solution. Doing the same for dynamic processes is something else. In principle, each step of the lineage is under CI/CD, so that each commit to a process triggers a change in the lineage of future data.

Accordingly, each datum should be mapable to a sequence of operations, each of which are versioned. This will enable us to reason about historical data.

## Problem

How should such data lineages be documented, and which processes should support it? In particular:
1. What are the requirements to metadata formats?
2. What are the requirements to interactions model?
3. How can we make a CI/CD pipeline automatically update the lineage documentation of produced data?
4. What would it tage to trigger invalidation of data produced by previous version of processes and regenerate it according to the newest revisions of the processes (at the lowest possible overhead)?

## Approach

## Related Work

