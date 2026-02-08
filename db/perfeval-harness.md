# Performance Evaluation Test Harness

**Tags:** performance evaluation, test harness, portability, platform independence

## Introduction

Measuring performance involves:
- Defining points and events of interests.
- Instrumenting code for logging when these events occur, and what the state is when they do.
- Mocking components outside of the system under instrumentation.
- Feeding in a workload at a well-defined rate.
- Measuring relevant performance characteristics and resource consumption.
- Logging these data.
- Postprocessing these logs to map workloads to KPIs (over time).
- Plotting the resulting data for sanity checks.

Part of that is to keep track of which processes make up the system, and how much CPU, memory and network they use. Plenty of open-source tooling is available for Linux, and some exist for Windows as well. Available metrics are different though. On OSX, access to the resource consumption of another process seem to have been blocked (for some sort of security reason, I assume). In reality, this means that we can't ask our students -- some of which are on OSX -- to do general-purpose performance evaluation in their projects.

## Problem

Is it possible to get around the restrictions on OSX (e.g., by beoming a privileged user), or would these students have to use a virtual machine?

What should a portable general-purpose performance evaluation framework for producing log files look like?

## Approach

## Related Work

