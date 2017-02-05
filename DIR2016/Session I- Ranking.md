# Session I: Ranking

## Axiomatic Result Re-Ranking

### A Brief Tour of Axiomatic IR

Research Goal: identifiy and formalize these properties as axioms.

Kemeny rank-aggregation scheme.

## Exploring Deep Space: Learning Personalized Ranking in a Semantic Space

Semantic spaces:

Man - Woman
King - Queen

Similar for items? Genre, etc

You cannot move movie genre and suspense at the same time.

Raise dimensionality: Allows to raise the amount of factors.

Hyperplane.

### Implementation:

Hierarchical Softmax

wordInImdbReview --> movieId

Sigmoid, Distance hyperplane, Hyperplane coefficients

Recall@10

## Inoculating relevance feedback against poison pills

Search is difficult, because we have a very small query. We can make it better by knowing a few relevant documents. Enrich the user's query by using a set of evaluated documents.

* Poison Pills: harmful relevant documents
* **Topic Drift** in the feedback model

Terms that are neither specifics nor general?

Super relevant op prominent words.

1. General model
2. Specific model
3. Significant Words model

### How to estimate SWLM?

Leuke wiskundige formule.

SWLM: specific word latent model

SWLM is het beste in het voorkomen van poison pills.


ICTIR 2017: Lots of machine learning.

Q&A

Q: Wouldn't it be better to detect poison pills and then disregard them alltogether
A: 

Q: Did you see any effect in a very specific query?
A: