# Bazel

Klaus Aehlig

For Google use-case: Large mono-repo, 10^4.5 engineers working on it 

* Optimized for large mono-repos
* Aggressive caching without losing correctness
* Declarative style of BUILD files

# How it works

* Load the BUILD files
* Analyze dependencies between targets
* from rules generate action graph
* execute actions

on subsequent builds, update the graphs

--- Example ---

