# A Universal Dependencies Treebank for Dutch

## Universal dependencies for dutch

* Can we use previous work for Dutch to produce UD-Dutch Treebank?
* Can we evaluate/bootstrap for UD-Dutch?

http://universaldependencies.org/

Parsey's Cousins (Syntaxnet)

Parser McParseface (Google)

## UD for dutch

v1

* Alpino treebank -> CONLL-X -> UD
* Many conversion issues, low quality

v1.3

* 65K sentences, mixed corpus
* manually corrected
* Wikipedia section converted automatically to UD
	* No need to redo manual corrections
	* silver standard can be created as well
	* evaluation UD-parser against Alpino (& conversion)

### Converting Dependency Trees

For each word, using Lassy annotation:

* Determine UD dependency label
* Determine the position of its head

## Lassy to UD Conversion

High-quality Automatic Conversion

All UD POS-tags and dependency relations can be assigned using only information that is present in the original Lassy annotation.

UD-LassySmall released (UD v1.3)

* train, dev, test split of 7.341 (Wikipedia) sentences from LassySmall
* v2.0 to be released end of February

https://research.googleblog.com/2016/05/announcing-syntaxnet-worlds-most.html



