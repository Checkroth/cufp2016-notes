# Intro
- Jasper Van der Jeugt
- Fugue
- Declare config in a DSL
- Server is set up and continuously reinforced / monitored

# DSL in the Architecture
- Conductor
- Can update, kill, monitor server
- DSL Inspired Haskell, Ocaml
	- Compiler written in Haskell

# Why we don't use YAML
- There are shortcomings
- Ansible - language isn't really composable
	- Can create trouble / be difficult to manage
- Scope and rules are not really clear
- Configuration defaults??? location not really defined
- Error messages unclear

# Design Goals
- Simple tasks should be simple
	- Need very low overhead
- Advanced things should be clean
- Not general purpose language

# Typed Language
- Looks like yaml, but actually typed
- Type inferencing or explicit typing
- Structural type system for records
- Scoped labels
	- Practical with simple rules
	- Improvement on scoped label disadvantages:
		- Extending record same as updating record

## Records & Patterns
- Update fields within fields
- update through constructors
- Records not enough - Abstraction needed
- *Functions*
	- Remove repitition
	- included with syntactic sugar
		- Traditional () for wide understanding
	- Various shorthands

## Named Parameters
- Not that easy in functional lang
- Use 'records' to give names to arguments
	- Keeps type inference and makes other interactions easier
- Problems/fixes with record usage:
	- None padding with coersions
	- Optional lifting
- Optional type gets special treatment, but the benefits are worth it
