# Acro(yoga) Graph

**Tags:** graph database, webapp

## Introduction

Acroyoga is a physical practice that combines elements from acrobatics, yoga and thai-massage. The practice has a therapeutical side combining yoga and thai-massage (call *lunar*), and a active side combining yoga and acrobatics (called *solar*). This project focuses on the solar side.

There a three roles:
- **Base:** Who is supported by the ground.
- **Flyer:** Who is supported by the base.
- **Spotter:** Who helps making sure that when things go wrong they only do so to an acceptable degree.

There are two styles:
- **L-Basing:** The base lies on their back (often with their legs straight up, thus forming an `L`).
- **Standing:** The base is standing up.

During the practice the flyer/base combo enters a number of *poses*. A pose can be described through the skeletal configuration of the participants and their contact surfaces. The practitioners may *transition* between poses. This makes the whole foundation a graph. A path (aka sequence of transitions) is called a *flow* and a cycle is called a *washing machine* (as you can keep on going round and round).

There is a large number of poses and transitions (and thus a mind-numbingly large number of potential flows and washing-machines). These all have names, and these names are often region specific. Both new and experienced acroyogis can have trouble remembering flows, and could use a tool for navigating this complexity.

Poses, transitions, flows and washing machines exists at varying difficulties. Practitioners come with a number of properties that influence how they experience those difficulties. This includes (but is not limited to):
- Mobility (e.g., outer rotation of left leg).
- Injuries (e.g., weak right wrist).

## Problem

A tool around an ever growing knowledge base of poses, flows, transitions and washing-machines is needed.
- How should the knowledge data be modeled in order to provide flexible querying options?
- What should the interface look like?
- How should elements from a user interaction (e.g., a washing-machine) be shared?

## Approach

Proposed approach:
- Interview with a number of acroyogis in order to explore the requirement space.
- Analysis to determine the relationships (e.g., dependencies and mappings) between the domain-relevant concepts.
- Design of a solution for the problem. Solutions based on RDF and a labeled graph database should be considered.
- Implementation of that solution.
- Evaluation through a combination of performance tests (e.g., how long does it take to load critical contents?) and user tests (e.g., do they like it?).

## Related Work

- [YouTube](https://www.youtube.com/results?search_query=acroyoga)
- [Join The Circus](https://jointhecirc.us)

