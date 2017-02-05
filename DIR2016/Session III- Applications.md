# Session III: Applications

## Evaluation and analysis of term scoring methods for term extraction

35 pages: Could have shown a term analysis of the paper.

Keywords or key terms: short phrases that represent the content of a document or a document collection.

Needed: term scoring (relevance/importance of terms)

### Introduction

* What factors determine the success of a term scoring method for keyword extraction?

5 methods applied to 4 tasks

Q:

* Influence of
	* Collection size
	* Background collection
	* Multi-word phrases

1. Generate candidate terms
2. - all word n-grams with n={1,2,3} that do not contain a stopword.

Central criterion for term weighting: frequency

Extended with other principles:

* Informativeness ('specificity'): term frequency relative to a background mode
* Phraseness: How strong ('tight') is the combination of words in a multi-word phrase.

### Methods

Informativeness methods:

* PLM: Parsimonious Language Models
* FP: Frequency Profiling
* CB: Co-occurrence based

Phraseness methods:

* C-value

Informativeness and phraseness:

* Kullback-Leibler Divergence for Informativeness and Phraseness (KLIP)

### Results for corpus size

KLP > C-Value > PLM > KLI > FP > CB

More words, phraseness becomes more important and better.

Aside: Gamma in KLIP stelt in hoe belangrijk multi words zijn, hoger is minder belangrijk (Verschilt per taal en domein, iets voor prominent words?)

### Conclusions

* Collection size
	* Larger collections lead to better terms
	* Best method for larger collections (> 10K words): KLIP
	* Best method for smaller collections (< 5K words): PLM 

The goal poses specific requirements on the extracted terms: terms that are informative for author profiling are different from terms that are powerful for query expansion.

## Siamese CBOW: Optimizing Word Embeddings for Sentence Representations

* From word-level semantics to sentence-levels semantics
	* We know how to get high-quality embeddings for words. How about embeddings for larger pieces of text?
		* Sentences
		* Paragraphs?
		* Documents?

* Evaluation task

Sentence similarity: find out if two sentences have the same meaning.

### The main idea

* Average the embeddings of words in a sentence to get a distributed sentence representations
* Directly optimize word embeddings for the task of being averaged
* Predict the current sentence from the sentences before and after it similar to what word2vec does with words. Sentences that have similar surrounding sentences should get similar representations.

Word embedding is het omzetten van een woord naar een vector. https://en.wikipedia.org/wiki/Word_embedding.

Sentence embedding is dus een hierarchische vorm van word embedding.

### Solving the softmax problem

In theory, we should do a softmax over all sentences.

This is all completely unsupervised.

## Unsupervised, efficient and semantic expertise retrieval (and beyond)

* What is expertise retrieval?

	* The task of finding the right person with the appropriate skills and knowledge wrt a topic.
	* More generally, an entity finding task.

### Beyond expertise retrieval

* The expert finding model falls in a more general class of Neural Language Models for Information Retrieval.

