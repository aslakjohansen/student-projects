# SparQL Query Visualizer

**Tags:** web, parsing, svg, web component, graph layout

## Introduction

At the Center for Energy Informatics we are running and continuously extending a fairly complex distributed system. We are using RDF-based ontologies for a significant (and growing) portion of our metadata needs. For instance, we have a [dashboard](https://dl.acm.org/citation.cfm?id=3281014) which only configuration is a link to a service hosting a model based on such an ontology. From this model, it automatically extracts links to floorplans, available per-room sensors and the data streams of these. When data arrives the relevant rooms are colored according the the value. Running the dashboard on a different building is a matter of pointing it to a model of that building. We use the SparQL query language to extract application-relevant information from this model. SparQL is a powerful language, but it can have a steep learning curve and at times need debugging. In this project we would like to reduce this burden by introducing a reusable web component that can visualize the query as it is being entered.

An SVG object can be manipulated from javascript.

## Problem

How to create a reusable web “component” -- preferably free of framework dependencies -- that can illustrate a SparQL query visually.

It should allow for the live updates as a user writes the query and have a functionality to store the result to disk as vector graphics.

Stretch goal: Define patterns and highlight pattern overlaps. One could even make suggestions to the query to make it “snap” to a pattern.

Stretch goal: Have one model of the query and two views for editing it: Textual and visual.

## Approach

Make a lexer and a parser (reuse if open source equivalents ones without dependencies can be found). 

Implement a primitive spring-based graph layout model. Stretch goal: Allow the user to drag a node.

Start out with pure JavaScript and see where it goes.

## Related Work

![Example of visualized SparQL](figs/sparql_pattern.png)

