# 	Session II: Users

## Predicting User Satisfaction with Intelligent Assistants

Metaphone representations
"WhatsApp" -> "WTSP"
"What's up?" -> "WTSP"

### Paper

Objective: Plan a drive to a vacation address using voice assistent.

Measure user statisfaction

Baseline: Train on only click features
Interaction model: Train on click touch and acoustic features.

#### Conclusion

* User satisfaction with search dialogues

* Measure different interaciton signals:

	* Click
	* Acoustic
	* Touch
* Significant gain over baseline

## Active and Passive Utility of Search Interface Features in Different Information Seeking Task Stages

Different title: "Clicked or Just Looked at?"

### Related work:

* Task-Based information seeking
* SUI


### Setup

User study (26 participants; 24 analyzed)
Task design: explicit multistage approach

SearchAssist

### Findings

#### Active behaviour

* Clicks

#### Passive behaviour

* Mouse movements not leading to clicks
* Eye-movement: Heatmaps
* Fixations

#### Perceived feature utility

## Beyond Actions: Exploring the Discovery of Tactics from User Logs

How do we compare user search behaviours between the two systems?

**Issues:** _comparability_ and _interpretability_

### Search log analysis: beyond actions

Abstract away from actions, instead look at tactics.

### Procedure for search tactic identification

* Action parsing
* Determine target tactics
* Action segmentations
* Tactic classification

### Target tactics

* "A move made to further a search"
* Our approach to determine a set of target tactics
	* tactics should be supported by the system
	* tactics should be identifiable from the log
	* tactics are at operational level rather than cognitive level (due to limited information recorded in our data)
	* Modified Marchionini's ISP model (1995):
		* "formulate query (FQ)," "execute search (ES)," "examine result (ER)," and "extract information (EI) + "Review history" (RV); "Organising results (ORG)"

### Lessons learnt

* Manual coding: accurate, but tiring, even with a dedicated labelling tool (yes, we made one)
* Heuristic rules: possible to derive a set of simple rules to achieve high accuracy (F1 > 0.95)
	* Rule coverage: depending on the log/system, user behvaiours turn out to move dirverse/regular
* CRFs based method: similar accuracy (F1 > 0.9) with a small training set (20% data) 

