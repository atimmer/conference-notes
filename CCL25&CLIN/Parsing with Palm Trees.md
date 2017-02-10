# Parsing with Palm Trees

* Charniak parser: 50 best trees
* Rerank according to LSTM-LM trained on millions of silver parse trees

LSTM-LM (LM: Language Model)

Palm tree: Linear representation of a tree

## Why does this work?

* Language modeling over Palm trees?
* LSTM?
* Silver trees, self learning?

Considerations

* Alpino
* Derivation palm trees
* Silver trees

Two experiments

* Reranking
* Palm score as additional feature in disambiguation

### Data

* Alpino baseline: 92.87
* rerank LSTM: 92.42
* rerank N-gram: 90.73
* random: 83.93