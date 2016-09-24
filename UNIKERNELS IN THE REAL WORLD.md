# Introduction
- "Baby steps to unikernels in production"
- Sean Grove
- VP Eng @ Pay Garden
- http://github.com/sgrove

# Caveats
- Talk reflects personal experience
- Subjective
- Mirage-specific

# What is a unikernel?
- Throw out existing os
- App becomes entire VM
- Only keep what app specifically needs
- Don't pay for anything you don't use
- STACK:
	1. Application code
	2. Mirage runtime
	3. Hypervisor

# Why unikernels for industry
- Lower resource usage huge plus
- High security
- Infrastracture simplified, improved flow
- Dev tooling
- Overally much more simple

# History of deployment
- Bare metal
- VMs
- Immutable infrastructure
- Continuous deployment
- ~ Repeatable, reliable, scalable infrastructure
	- Mirage: _Super immutable_
- Great for pay garden, tiny tiny team + simple infrastructure = very nice

# Getting to Unikernels
- Mirage can first be built as unix application
	- Get to market much more quickly
- Switching to unikernal, can no longer depend on unix
	- Often unix dependencies added during development
	- Need to be careful not to do this if you plan to move to unikernel

# Unix -> Unikernel
1. Prototype
2. Production
3. Next Gen

## Prototype
- Artisanal
- Artifacts hand crafted
- Infrastructure tailored and crafted for application
- Difficult to deploy
	- Lots of underlying complexity to learn
- Difficult to monitor
- Not easily scalable
	- All very manual
## Production
- Automated builds
- Automated deployments
- Reuse existing infrastructures
	- Public hosting
	- Monitoring
	- Scaling
	- Important to be usable in existing infrastructure
- Dependency management
	- Major issue for reliability
	- Unsolved challenge
- Environments
	- Also unsolved
	- Mirage supports many backends
	- Maybe docker, but some issues
- Hosting
	- AWS - Deploy 30 mins manual work
	- KVM - Google compute engine
	 	- Primitives match very nicely
	 	- Load balancing / logging / deploying very easy
- CI/CD Pipeline
	- Build unix backend & run tests
	- Build & upload Solo5 artifact
	- Zero downtime update if on production branch (master)
## Next Gen
- Current infrastructure limiting
- More unikernel aware
	- Boot very quickly (<100ms)
- Faster boot times
	- Boot instance for request - kill when finished
	- Per 100ms billing
- Easier rollbacks
### Concerns for Adopting in Production
- Documentation
	- Particularly bad for OCaml
- Community
	- Niche, small
	- MailingList/IRC compared to Stack Overflow
	- Future of Mirage unclear (Tool? Research?)