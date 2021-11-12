# Mesh-Networking over LORA

**Tags:** lora, wireless, mesh, network, distributed systems

## Introduction

LORA has the potential to communicate efficiently over both long and short distances. A mesh network on top of LORA would highligt a number of tradeoffs which -- if resolved correctly -- might result in an incredibly flexible and adaptible infrastructure.

## Problem

Implement a multi-gateway mesh networking protocol on top of LORA trancievers.

## Approach

**Potential detail:** Large scale evaluation could be simulated using something like TOSSIM og simply creating a soft network substrate that can be linked to several instances of a firmware binary.

## Related Work

- [Hackaday: 
LoRa Mesh Network With Off-the-Shelf Hardware](https://hackaday.com/2020/02/26/lora-mesh-network-with-off-the-shelf-hardware/)
- [LoRa Mesh Networking](https://github.com/nootropicdesign/lora-mesh)
- [Route Poisoning and Count to infinity problem in Routing](https://www.geeksforgeeks.org/route-poisoning-and-count-to-infinity-problem-in-routing/)
- [Eventual consistency](https://en.wikipedia.org/wiki/Eventual_consistency)
- Low-Power listening:
  - [TEP 105](https://github.com/tinyos/tinyos-main/blob/master/doc/txt/tep105.txt)
  - [Optimal Routing for Time-Driven EH-WSN under Regular Energy Sources](https://www.researchgate.net/publication/329132570_Optimal_Routing_for_Time-Driven_EH-WSN_under_Regular_Energy_Sources)
- [TOSSIM: Accurate and Scalable Simulation of Entire
TinyOS Applications](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&ved=2ahUKEwic1em3sJTtAhVeCRAIHZWEDREQFjAAegQIAxAC&url=http%3A%2F%2Fcsl.stanford.edu%2F~pal%2Fpubs%2Ftossim-sensys03.pdf&usg=AOvVaw3aRtptJUCB1WFwYgLpol0R)
