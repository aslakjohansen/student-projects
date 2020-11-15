# Make Media Credible Again

**Tags:** web, graph, directed acyclic graph, dependency graph, dependency analysis, cluster analysis, fragility

## Introduction

During the last decade or so, and the previous two US elections in particular, the credibility of online media has taken a dive. It has gotten so bad that there is no longer a shared sense of reality, and that has severe democratic implications.

## Problem

We would like to create a system that allows us to track the premise graph of information (e.g., news), and offer validation through:
- peer review based on user preferences rooted in a social network. In other words, users will credibility scores based on functions over their own set of trusted references. This makes the score subjective, and that subjectiveness should be observable through cluster and fragility analysis.
- cycle detection. This to highlight that an "argument" is cyclic in nature and thus invalid.
- subgraph invalidation when a premise is debunked. When a premise is found invalid all statements relying on it (without) an alternative reference should be invalidated. In practice this means that a notion of reference equality needs to be introduced so that two reports of the same incident are linked in case the incident is found to be fake.
- subscription to invalidation. So that users get notified whenever a document that they have consumed is found invalid.

It should be able to coexist along existing sources and offer a path to integration in a distributed manner (e.g., CNN should be able to participate by adding markup to their pages).

It should keep a history of all indexed documents so that revisions figure as a first-class citizen in the modeling: One revision may be invalid and another valid.

What would a system like this look like?

## Approach

Come up with a way of annotating an HTML document so that a statement may (i) be referenced and (ii) reference other such statements. The latter part should support alternatives in case of a source being pulled.

Build a platform that stores the dependency graph, and allows the required operations on it.

## Related Work

Research databases keep track of references, although is is not always clear exactly which statements are supported by which references. This is especially true when the consuming party is a machine. It is thus practically impossible to invalidate a finding if a segment of the chain of supporting references are found incorrect. Still, these have an existing reference system. Examples:
- [ACM Digital Library](https://dl.acm.org)
- [IEEE Xplore](https://ieeexplore.ieee.org/Xplore/home.jsp)
- [Google Scholar](https://scholar.google.com)

There is within the area of proof systems a logic for describing the steps that goes into a solid argument. This could give inspiration to the modeling of how references depend on each other.

A true graph database could be a good way of storing the data.

