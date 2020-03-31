# Access Model Based on Queries Against an Ontology

**Tags:** access control, ontology, blacklist, whitelist, access model

## Introduction

Access models are typically defining access either on individual locations or via blacklists and whitelists using patterns on locations.

The approach of individual locations becomes next to useless when applied to an evolving model based on an RDF-based ontology. The patterns of a blacklist/whitelist approach naturally translates to a query.

## Problem

How can we add a sensible access model to the interface of an RDF database that allows us to store secrets in the model and control who has access to them?

## Approach

The envisioned approach:
1. Wrap an RDF library to construct an RDF database
2. Add a user model, mapping each user to two sets of queries representing a whitelist and a blacklist
3. Enforce restriction of access based on these lists
4. Evaluate solution
5. Propose idealized solution (e.g., involving modifications to the query engine component)

## Related Work

