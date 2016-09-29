# Introduction
- Jet
- New york based E-Commerce
- Purchased for 3.3 Billion after 1 year
- 90% of backend F#
- Heavy microservice focus
	- 500-1000 microservices
- #4 marketplace worldwide
- Intending to compete with amazon
- People
	- Rachel Reese
	- Nora Jones

## Testing
- Manual testing will miss parts
- VW - No chaos testing => not good
- Important to test that interactions work in your environment

# Why F#?
- Simon Cousins quote - bugs don't come in
- TickSpec - BDD Testing Project in F#
	- Much less dependency growth
- Stack overflow survey
	- Most Loved Languages - F# is third
	- Lots of love for FP

# Chaos Engineeringとは
- Controlled experiments to see what is going to go wrong
- Build confidence in ability to tolerate failure
## Principles
- Define 'normal'
- Assume 'normal' will continue in control & chaos
- Introduce chaos
	- Crash servers
	- HDD malfunction
	- Network failures
- Analyze behavior between control & chaos

# Benefits of Chaos
- You're awake
	- Its controlled, not at 3am
- Designing for failure
	- Knowing something will go wrong -> design system to account for it
- Healthier systems
	- Systems designed to handle failure before failure occurs
- Self Service
	- Encourage engineers to design strong systems

# Chaos Testing Examples
- "Chaos Monkey"
	- Netflix
	- Easily #1 in chaos testing world
- That's it, really

# Jet is Different
- Not testing in production
	- Yet
	- Working their way up
	- It is important to be testing in production
- Using Azure and F#
	- Not really covered by other products