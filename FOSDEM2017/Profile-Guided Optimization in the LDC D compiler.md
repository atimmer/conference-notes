# Profile-Guided Optimization in the LDC D compiler

Simple idea: I can optimize better if I have more information.

Basic concept: You create a profile of a running application and do optimizations in the compiler based on this.

If the profile doesn't fit the use case it can result in worse performance.

D-language

## Implementation in the LDC compiler

* Inserts calls to LLVM intrinsics

## What kind of optimization is done with this?

* Indirect calls occur very often in OO languages (virtual functions).
* If a 'likely' called function is known then an optimization is to check for the 'likely' function and call this function directly.
* PGO helps to find the 'likely' called function.
* Enables further optimization, e.g. function inlining.

## (my) conclusion

You can do a ton of optimizations using profiles by optimizing your code yourself, but in more lower level language some optimizations are only possible by the compiler. So then this technique is useful.