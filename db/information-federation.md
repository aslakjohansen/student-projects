# Information Federation

**Tags:** federation, property graph database, adapter, dsl

## Introduction

Property graphs are expressive enough to fulfill most modeling needs, and property graph DBMS can operate at reasonable rates. So, there are lots of data that makes sense to place withing a property graph DBMS. However, some subset of the data that one might want to query may be governed by a 3rd party, and because of this we cannot import it. It might not even be available to us in as a property graph, but perhaps as an RDF store or relational data.

Traditionally, this would be solved by querying each source independently, and then writing some logic for postprocessing all these results into a single resultset. This is not particularly convenient though, and can have a significant negative impact on resource consumption (multiple temporary resultsets that can't be reduced due to cross-silo dependencies have to be manifested).

However, if a property graph DBMS allows us -- through an extension of sorts -- to inform how parts a query is resolved, then this can serve as a foundation for federation. 

## Problem

The goal of this project is to explore what can be achieved by extending an established property graph DBMS in terms of federation. Specifically:
1. What kind of extension opportunities are available to different property graph DBMS?
2. How can each of these help us resolve part of the query against a remote DBMS?

## Approach

There are three obvious approaches (if supported by the property graph DBMS):
1. Create special nodes and/or edges that cab be inserted and act as links to remote representations. They inform the graph traversal algorithms used by the query execution engine, and perhaps even fulfill parts of the the query resolution.
2. Create a frontend that parses the query, and splits it up into subqueries. Each subquery is then executed in a context that may depend of other subqueries. Each subquery can potentially be resolved in a different store.
3. Combine a number of queries (potentially against different stores using different query languages) with logic (following a custom DSL) that links the results together.

There is a number of relevant property graph DBMS:
- [Neo4j](https://neo4j.com)
  - Some relevant [documentation](https://neo4j.com/docs/java-reference/current/).
- [Memgraph](https://github.com/memgraph/memgraph)
  - Some relevant [documentation](https://github.com/memgraph/mage).
- [Titan](http://titan.thinkaurelius.com)
- [OrientDB](http://orientdb.org)
- ...

**Note:** I do not know to which degree this is possible, so that would have to be explored beforehand.

## Related Work

