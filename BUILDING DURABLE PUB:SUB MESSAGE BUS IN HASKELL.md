#Intro
- Will Sewell
- Platform engineer at Pusher
- [Slides](goo.gl/ULJq6X)
- Will talk about garbage collection

# Pusher とは
- Hosted web socket API
- Users publish using http
- Users subscribe via web sockets
	- Recieve messages via this
- Based on Redis hub/sub

# The problem
- No state
- Brief Loss of connection => Will never recieve message
- Need to keep cache / message queue
- Need to handle >10,000 / second to be affordable
- Latency must be <50ms (Publish => Subs)

# Why Haskell?
- Made before speaker joined company
- Legacy written in Ruby
- After codebase grows, start to crave haskell
- Like simple languages with hard principles
- Fast

## Pros / Cons of Haskell
_Just speaker's opinion_
### Pros
- Types, good for correctness as well as design
- Concurrency Model
	- Green threads, STM
- Great tooling
	- Threadscope
	- Heap visualization
	- Stack
- Hiring
	- Lots of high quality candidates
### Cons
- No standard way of solving problems
- Lots of competing solutions
	- Strings vs Text
	- Pipes v Conduit
- Error messages
	- Abstractions leak
	- Need to understand lots of underlying concepts
- Tooling limitations
	- Some are good, but limited options and often clunky
	- Not living up to potential, tools could be so much better

# The Message Store
_Problems with Garbage Collection_
- Messages constantly inserted and removed from store
- Garbage collection blocking application from running
- Max pause time proportional to size of working set

## GHC GC Design
- High rate of un-referencing
- Most objects die young
- Generational
	- Heap split in generations
	- Long-term objects exist in 'old generation' heap
	- Checked infrequently
- 'Stop The World'
	- Application blocked while heap being checked

## Worst Case
- Message Store has long and equal life times
- All objects in old generation

# Solutions
- Write storage in different language
- Write program in different language
	- Re-wrote program in Go
	- Production raft libraries
	- GC Specifically low latency