# Variance Detection in Graph Databases

**Tags:** graphs, databases, diffing

## Introduction

Graphs are often used to describe physical setups. For example, Energinet has a large amount of ​​hardware distributed across stations spread around the country. These stations are all slightly different, and these differences can be used to explain observations. But to do this, you need to be aware of how they differ.

This project aims to construct a tool to find such differences. For example, you could imagine a graph of a computer where a motherboard is connected to 1-* CPU, 1-* RAM and 1-* SSD. When you then have a database of computers, you can choose to see them as a class and analyze what such a class looks like. It could be something like a computer typically has 1 CPU, 2 RAM and 1½ SSD. You can then compare specific computers with this. If you then come across one with 7 SSDs, you can expect it to behave differently in the data streams you have about it. This is a gross simplification though.

In practice, it shouldn't be about numbers (it should be about shape, and maybe also properties), and it shouldn't just be about a single level (for example, you could be interested in which monitors are connected to which graphics cards are connected to the motherboard). What we're after is basically an equivalent of a visual diff viewer; just for graphs where one graph is some kind of representative of a classification. It's not that I find this computer domain particularly interesting, but there are similar issues at, among others, Energinet.

## Problem

## Approach

## Related Work

