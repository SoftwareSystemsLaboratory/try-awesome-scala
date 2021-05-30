# try-awesome-scala

A collection of scripts showing how to use the best of Scala. These scripts are *not* intended to be practical but *are* intended to show how to use the library/component in question. Our primary focus is on programming libraries. However, libraries with GUI or visual outputs may be included, provided a minimal script can be written to show their usage.

# Rationale

Recipes are useful for learning to be productive in any programming language.
For just about every language, there is an "awesome" collection that highlights the best libraries and tools for each language.
e.g. [awesome-scala](https://github.com/lauris/awesome-scala) 

A critical aspect of being "awesome" is to make it easy for people to do the following:
- get started with a minimum viable example (MVE) or application (MVA).
- know that "awesome" remains awesome; many awesome packages subsume others.
- have some assurance that an "awesome" package is being kept up-to-date
- ...among other reasons, some of which are related to computer security

# How to contribute

- Download and install the Ammonite REPL. All contributions to `try-awesome-scala` are expected to be concise and clear scripts. Presently, Ammonite is the exemplar when it comes to Scala scripting. (It's *awesome*.)
- Create a unique (new) foldler name for the awesome project you want to include in `try-awesome-scala`. Do not create deep folder structures. 
- Create a script named try-*whatever*.amm that uses `#!/usr/bin/env amm` as the shell and make it *executable*.
- Use Ammonite's `Ivy` import syntax. You can see examples of this in any of the existing scripts.
- Your *try* script may have any number of entry points but must be able to run as an executable with proper *parameterization*. This means there will be command-line arguments. Again, see other scripts for how to annotate your various entry points to include command-line arguments.
- We strongly encourage contributions that respond to an *issue* where we are seeking first-time contributors. 

# Some thoughts on Scala style

- Err on the side of clarity. Conciseness is often the enemy of clarity and--given Scala's `val`--is rarely more efficient. Compilers really do know how to optimize code.
- Document all *implicit* behavior in your script. Implicits are powerful, but they often *impede* comprehension in Scala code. 
- Avoid anonymous variables, e.g. `_`, whenever possible. Yes, you can do `1 to 10 map { math.pow(_, 2) }`. But `1 to 10 map { number => math.pow(number, 2) }` actually reads better at no loss of generality or performance. And we note that `_` can be used in a multitude of situations. Unless there is a good reason, avoid.
- Use *descriptive* variable names, except when obvious. We don't mind if your comments are limited, but if you cannot make good choices when it comes to naming variables, functions, types, etc., comments are a must.
- Break up complex statements into multiple lines. Don't hesitate to introduce `val` definitions in liew of more lengthy expressions.


