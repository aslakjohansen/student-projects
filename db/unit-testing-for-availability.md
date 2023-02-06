# Unit Testing for Availability

**Tags:** availability, unit testing, actor model, supervision tree

## Introduction

On the surface of it, testing for availability requires time. Lots of time. However, different approaches can be taken. For instance, we could explore what the consequences of a single component failure is, for all components. That will, additionally, tell us something about which components are most critical (to availability). This approach is especially relevant if an actor model approach is followed with supervision trees.

## Problem

To which degree can unit tests be used to test for availability of software that is build using the actor model, and what woiuld a framework for doing so look like?

## Approach

Each actor type has to be associated with unit tests that explore what happens to a number of metrics (KPIs) when an instance of this actor type dies.

## Related Work

