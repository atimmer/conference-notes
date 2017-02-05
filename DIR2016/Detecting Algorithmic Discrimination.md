# Detecting Algorithmic Discrimination


## Part I: algorithmic discrimination concepts

Motivation and examples of algorithmic bias
Sources of algorithmic bias
Legal definitons and principles of discrimination
Measures of discrimination
Discrimination and privacy

A dangerous reasoning: Algorithmic inputs include only objective elements. Hence, they cannot discriminate?

Results for "CEO" in Google Images: 11% female, US 27% female CEOs

Self-perpetuating algorithmic biases

Algorithms are "black boxes" protected by several things.

Weapons of Math Descruction (WMD)

Two areas of concern: data and algorithms

* Disparate treatment: Treatment depends on class membership
* Disparate impact: Outcome depends on class membership (Even if (apparently?) people are treated the same way)

### Proving discrimiation is hard:
* The accuser must produce evidence of the consequences
* The defendant must produce evidence that the process was fair

This is the criterion of the European Court of Justice

### Principles for quantifying discrimination

Two basic frameworks:

* Discrimination at the individual level: Consistency or individual fairness
* Discrimination at the group level: Statistical parity

### Discrimination and privacy

If you remove the source column (e.a. gender) and add the outcome. Then if you can reverse engineer the source column you are discriminating.

## Part II: algorithmic discrimination discovery

### Discrimination discrovery task

Given a large database of historical decision records, find discriminatory situations and practices.

#### Data miing approaches

##### Classification rule mining

Which are the groups that are potentially discriminated.

* Check direct discrimination, A, B -> C
* Indirect discrimination

"It seems you would also discriminate, turns out these algorithms look for stronger discramintory practices."

##### k-NN classification

Nearest Neighbours

* Situation testing:
	* Legal approach for creating controlled experiments
	* Matched pairs undergo the same situations, e.g. apply for a job
		* Same characteristics apart from the discrimination ground

### Discrimantory rankings


### Concluding remarks

1. Discrimination legislation attempts to create a abalance
2. Algorithms can discriminate
3. Methods to avoid discrimination are not "color blind" (A fair algorithm has a bias for the unprotected group)
4. Group fairness (statistical parity) vs. individual fairness.