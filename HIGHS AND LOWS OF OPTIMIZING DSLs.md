#Intro
- Jacob Stanley
- Icicle (?)
- Work at Ambiata
	- Use simple models to predict the future
	- Costs more to run code than to develop
	- Correctness more important than performance
	- Optimized DSL

# Icicle
- Query language for time-series data
	- `latest 5 in mean value` <- Example icicle query
- Three optimizations!

# Schema Specialization
- Code is I/O Bound -> its 1996?
	- 1800 MB/s sequential reads on macbook
	- Fastest ssd is 3300 MB/s sequential reads
	- You are not I/O bound - you're just slow
- Parsing performance matters
	- Avoid reading one byte at a time
	- (Read multiple at a time)
## The perfect parser
- Exploit what we know about "THe Scheme"
	- ASD|lang|{"sh: true"}|2016-01-01\n
- Memchar
	- `Data.ByteString.elemIndex` in haskell
- The scheme contains well known information
	- Strings are just lists of 64 bit integers
- Buffers always padded with 8 bytes
- *Read multiple bytes at a time*

# Partial Evaluation
- icicle is _pure and total_
- Beta reduction
	- Process of applying lambda to an expression
- Constant folding
	- Evaluation of constants and operations at compile time
- Icicle source -> Icicle core
	- Things are compressed / inlined
- PE Bottom up
- Beta reduction & Constant folding done at the same time
	- Lambdas are removed
	- necessary to compile to C

# Melting Down Data
- Records melt down to individual values
- Arrays melt down to individual arrays
- Options melt down to individual values + is some bool
- *Unpack* - extract melted value (?)
- *Pack* - Smash melted values back together

# Optimization Opportunities
- Eliminating dead code
	- Only using high values
- Eliminating compound types
	- Can be easily / quickly compiled to C