# Intro
- Ludovic Courtes
- Scheme, not typed language (kind of rare at CUFP)

# Guix
- Free software movement
- Deploy software using purely functional paradigm
- GuixSD - Guix System Distribution
	- `guix package -i guile`
	- `guix package -r guile -i python`
	- `guix package --list-installed`
- Environment Variables suggested on install
- Stores generations
	- Packages and install histories are managed and can be viewed / restored
	- `guix package --list-generations`
	- `guix package --roll-back`
- Scheme configuration file
	- Don't really need to know scheme to use though
	- `guix system build schememachine.scm`
- Can run configurations in servers / vms
- Deployments etc.

# Why?
- _Is there a package manager for neural networks?_
- Lots of language-specific package managers
- Almost every programming language have their own package managers
- This is good for development, but difficult for system management
- Language-specific PMs often assume things that aren't necessarily true about your environment
- You want states of machines to be the same across distributions

# Functional Package Management
- build process is a pure function
- Software built with this function is an immutable value in a graph of packages
- Builds are stored in hash of _all dependencies_

# Scheme All The Way Down
- Configurations scheme all the way
- Package manager all scheme
- Scheme determines packages and how they build and their dependencies and how _they_ build
- Scheme all the wawy up to OS declaration level

# Summary
- Distro and tools as scheme libraries
- Hackable through uniformity
- Using code staging capabilities to glue it all together


https://gnu.org/software/guix