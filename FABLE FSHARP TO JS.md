# Introduction
- Speaker wrote "Fable", which compiles F# to JS
- Other f# => js compiler first compiles to .net binary (?) and then goes through other steps
- Fable is straight from f# to JS
- F# Syntax similar to OCaml
	- Intentionally
- Even if you hate JS, the community is too big
	- For web dev, not using JS tools is a huge handicap
	- Working functionally while still being able to use JS tools is the main point
- Also has TypeScript parser
	-ts2fable
	- not perfect, sometimes need to manually edit after generating bindings

# Other
- Tomas Petricek
	- http://tomasp.net/
	- "The Gamma Project": http://thegamma.net/
		- New ways of data visualization
		- Keep data alive
		- Let users interact with the data
- Redux dev tools
	- https://github.com/gaearon/redux-devtools
	- Looks really cool
	- Very useful for debugging, qa
	- Can export steps to reproduce issues easily

# Hello World
- Have hello-world.fsx
- Use fableconfig.json for project settings
- npm init => generate package.json
	- (Running with Node, Mono)
	- (IDE is Visual Studio Code)
- _EVERYTHING_ is JSON
- Run `npm run build` to execute / run

# Testing
- Can use plugins
- Can use NUnit, other JS test suite

# Further Work
- "WebPack" not in great detail
	- Bundles our work so we don't have to explicitly load every file at runtime
- React bindings
	- Following web component standards (?)
- Redux
	- _Supposed_ to be functional programming
	- Cool development tools for state management
- Todomvc
	- Not really sure what this is about
- All tools used are well-documented in `components.fsx` in `todomvc-react`

# Live logic changes
- `npm run build-debug`
- `npm start debug`
- Can update code / change logic without losing state
- Good for testing state-dependant jawns

# Desktop applications
- [Electron](http://electron.atom.io/)
- Fully JS multi-platform desktop applications
- Running on chromium base, but not a web browser
- Driving force behind Atom editor
