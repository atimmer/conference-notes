# Session IV: A Mixed IR Bag

## Power Analysis for Interleaving Experiments by means of Offline Evaluation

### Evaluation in IR

* Offline evaluation
	* Allows systematic and repeatable evaluations
	* Usersa nd assessors do not agree
	* Relevance changes
	* Users do not agree with offline measures
* Online evaluation
	* Reflects the reality
	* Is expensive to conduct

* How to design an experiment?
* Power analysis in offline evaluation
	* The difference to be detected
	* The variance in the measurement
		* Estimated using historical data
* In online setting
	* We do not have historical data

## Content-aware Crowdsourcing Vote Aggregation

### Outline

* Past work
	* Exploiting Docuemnt content for vote aggregation

* Ongoing extensions
	* Crowdsourcing in extreme budget contrainsts
	* Information theoretic approaches
	* Experiments and results
	* Conclusion

Problem statement: Given a set of relevance assessments, how accurately can we infer the relevance of unjudged Web pages?

## Document Filtering for Long-tail Entities

* Context: construction and maintenance of knowledge bases and knoledge graphs
* Role of document filtering
	* suggest documents for citation in KB
	* select documents for KG triples extraction
* Document filtering for entities
* Output in KBA setting: P(rel|d,e)

### Background

* Entity-dependent and entity-independent models
* State-of-the-art is entity-dependant
* Most approaches rely on extrinsic signals
	* Wiki page views, tweets, queries, document burst
	* Related entities
* Approaches for head entities are ill-suited for long-tail entities
	* Limited/no Wiki page, slower burst, no known related entities..

* A document filtering approach tailored towards long-tail entities
	* Entity-independent
	* Relies on rich intrinsic, i.e., "in-document" signals

### Addressing the challenge on long-tail entities

* Informativeness
* Entity-saliency
* Timeliness

### Informativeness

* An entity profile should be udpated when a document changes one or more aspects of the entity
* Capturing informativeness with aspect models
	* **Build aspect models**
	* **Analyze and represent** document based on the constructed aspect models
	* **Sources** of aspect model considered: Wikipedia, open relation extraction pattern, closed relation extraction schema.

