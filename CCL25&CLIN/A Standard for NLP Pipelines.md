# A Standard for NLP Pipelines

## Problems

(With writing custom scripts for everything)

* Code duplication
* Software portability
* Research reproducibility and provenance tracking
* Reuse of existing software

## Common Workflow Language

http://www.commonwl.org/

* Common format for data analysis
* Community based standard
* ...
* Supports use of contains

* Processing step
	* Wrapper around a command line tool
	* Can be inside a Docker container
* Workflow
	* Sequence of processing steps

-- Example --

* YAML "Human readable"
* Flexible
* Extensible

## CWL for NLP

* Create CWL steps for tools
* Facilitate connecting inputs and output of these tools
	* Conventions for text processing steps

* NLP steps are generic (or at least we treat them like that)
* Inputs: [meta_in], in_files
* Outputs: [out_dir], [meta_out]

## nlppln

* Python package to create NLP pipelines using CWL

https://github.com/WhatWorksWhenForWhom/nlppln

## Example

(Frog) https://languagemachines.github.io/frog/

## Conclusion

* CWL + nlppln = a standard for NLP pipelines?
* Make your tools available as command line tools!