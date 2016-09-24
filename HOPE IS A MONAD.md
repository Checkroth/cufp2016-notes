# Intro
- Michael Sperber
- Retrospective talk
- Wanted to improve systems with freelance

## Bank
- Worked at german bank using scheme 48
	- Sperber maintained scheme 48
	- Wasn't actually hired to work in scheme 48
- Quotes to Derived Market Data Something something something volatility surface
	- C++
- Decorator Pattern for dynamic subclassing
- WHole bunch of issues
- Double/triple shifting
- Very trivial function
	- Implemented even in OOP easily
	- Lesson learned multiple times in professional life

# Semiconductor Creatinonscheduling
- FAB is very fickle
	- Semiconductor takes thousands of steps to make
- Lots of things changing at any given moment
- More like cooking than procedural process
- Program mostly makes 'suggestions' to FAB
- Hope that FAB does what want it to
- Types of Hope
	- Plain Hope - can't do anything
	- Hope with instructions - sometimes doesn't happen right away
	- Follow up hope - make sure its doing the thing
	- Shattered hope - :(
	- When you draw it out -- _HOPE is a MONAD_
- Purely Functional FAB
∂ -ƒ-> ß

# MVC & GUI
- `model -> model'`
- `view -> view'`
- Spaggetifies everything
- Infinite loops you need to handle
- React is close to functional
- [Reacl](https://github.com/active-group/reacl) with ClojureScript
	- Application state
	- Separate GUI logic from Application logic

# Distributed System
- Exchanging configurations among tablets based on physical location
- Transfering between systems
- Synchronization
- Utilized merkel trees
- F# Merkel trees
- Fully functional algorithm to implement this (synchronization)
- Very easy to test
	- Quickcheck
## Issues
- Auto-config printers
- Mounting drives
- Track changing environment
- Keep gui in sync
- ^^^^MUTABLE STATES^^^^

# Functional Programming Is Always Better
- OO as seen by an FP programmer
	- If the grass is greener on the other side, there is probably more maneur over there
- Purity
	- Even in applications that are inherently stateful
- Systematic Programming
	- Also mentioned in "Teaching Functional Programming"
- Type-Based Programming
- Static Typing vs Dynamic Typing
	- Static makes it very difficult to be systematic