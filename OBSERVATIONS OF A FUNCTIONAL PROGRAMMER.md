#Intro
- Yaron Minsky
- Coming to CUFP from 10 years ago
	- CUFP was basically only FP platform
- Now lots of FP talking platforms

# Three Pots (of Knowledge)
- Professional Experience at Jane Street
- Connections to other FP industry professionals
- Academic Functional Programming

# Two Worlds / Three Ideas
- World 1: Lisp Languages
	- like Racket
- World 2: ML Languages
	- like Haskell, F#
- All functional programming languages decend from one or the other.
- Big Idea: Pure Computation / Immutability
	- ML: Types (important concept in Haskell/Ocaml/F#)
	- List: Macros (Syntactic Transformation)
	- ML's style is more common

# Functional Programming is Not Popular
- Despite being the origin of many important concepts
- Lisp: First Garbage Collection
	- Now in _every_ language
- Technology and concepts from FP often adopted in other languages
	- These ideas are adopted with only partial understanding

# Functional Programming in the World
- We should not be satisfied at current level
- Applied FP concepts often "Lipstick on a Pig"
- FP _is_ good for general purposes
	- Current limitations are bad and unnecessary
	- (Limitations in applicable areas of use)
- (Unfortunately) little to no evidence that FP is good or better than imperative
	- Only way to prove FP is good is SCALE
	- Impelment on a large scale
	- Not just a couple large systems, but common commercial use on a large scale
- People cannot evaluate what the do not understand
## The Right Tools
- Popularity does not equal Quality
- GADTs are good for optimization
	- _note: I think this bullet is out of place_
- Be understanding of other programming environments
- Use the right tools for the right job
	- Mistake 1: "We need lots of tools for lots of systems"
	- You do not need so many tools.
	- Google limits to 4 languages
		- C++, Java, Python, Go
- When you (the engineer) pick tech or tools, think what that means for your organization

# Minority Languages
- Minority language means poor or small set of tools / libraries
	- Using a language is a contract to improve it
- If you depend on a technology, you MUST contribute back
- Minority languages tend to have small but skilled set of programmers
- Incremental and reactive programming
	- Iacademic perspective is valuable

# Teach Programming!
- Teach kids programming
	- With text adventures!
		- ([Side note: Yaron Minsky shared an example of this on twitter](https://bitbucket.org/yminsky/tiny-adventure/src))
- Your involvement in Programming means you should care about its education

# Q&A Notes
- Minsky thinks monorepos are very good
	- Unfortunately, OPAM doesn't work well wtih monorepos
- To switch a massive organization's main language / structure
	- Don't, and start your own company
	- Personalyl undertake the impossible task of making the switch
		- (Basically impossible)