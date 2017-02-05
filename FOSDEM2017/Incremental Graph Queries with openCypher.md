# Incremental Graph Queries with openCypher

Good explanation about Graphs using trains. Showing queries for proximity detection and for detecting "trailing the switch". Every step of the train the query has to be executed. The solution for this is incremental graph queries.

The Rete algorithm: Indexes the graph and caches interim query results.

Batch queries: Query results obtained on demand.
Incremental queries: Query results are always available.

## Incremental query engines

In the past there have been many implementations: CLIPS, Drools, VIATRA.

openCypher is an open specification of Cypher (query language)

## Incremental in openCypher

Convert query constructs to relational algebra.

ingraph: An incremental, in-memory graphy query engine

openCypher query -> Query syntax tree -> Relational algebra model -> Rete network model -> Rete network

Executed using Scala 😁

https://github.com/ftsrg/ingraph
https://github.com/ftsrg/trainbenchmark
https://github.com/ftsrg/bme-modes3