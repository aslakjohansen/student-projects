# Graf-Based Energy Balancing

**Tags:** control systems, distributed systems, graphs, energy balancing

## Introduction

Previous models for balancing the electricity grid have been based on the large copper plate model (where it doesn't matter where consumers and producers are). But in practice, the electricity grid is more complicated. It is a graph of wires, where an edge represents a wire with a number of characteristics (voltage level, original capacity, degradation). The nodes are transformers, fuses, power plants, wind turbines, households ... With the large copper plate model, one has to accept a risk that a small wire ends up having to carry a load it was not designed for.

## Problem

What would we be able to do with a more complex model of the electricity grid? Can we implement a more local balancing that takes into account the practical capacities of the cables. How should such a system be designed? What core issues need to be solved before it becomes a real possibility? What failure scenarios will there be in such a regime?

## Approach

## Related Work

