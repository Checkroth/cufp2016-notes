# Introduction 
### Building web apps with continuation Monads
- Introduction of DWANGO, Niconico, and account system
- Problems of component technologies of existing web frameworks
- Constructing web applications using continuation monads
- Updating components using continuation monads

# Introducting DWANGO and Niconico
- DWANGO company that operates video sharing
- Niconico has 50 million accounts
- Most major streaming service in Japan
## FP in DWANGO
- Dwango has adopted FP
- Using variety of languages
	- Scala
	- Erlang
- Speaker joined as scala specialist
- Wrote github.com/dwango/scala_text
## Account System
- Variety of services in Dwango
	- e-books
	- Slide services
	- video /live streaming
- User info is aggregated in account system across platforms
- Tasks
	- registration
	- authentication
	- updating user info
- Required interfaces
	- Want component tech to decompose application
	- doFilter
	- Servlet Request
	- Servlet Response
	- FilterChain
	-(Speaker gave examples here)
#Problems with Component Technologies
- Filter method doesn't have much info on type and parameters
- Don't necessarily know what kind of parameters will be passed
## Introduciing continuation monads
- Continuation represents rest o computation at any given point int he execution
- A: Given point. R: Result. `a -> r`: Remainder of function (?)

More specific information found here:
http://www.haskellforall.com/2012/12/the-continuation-monad.html

##Stray notes
- Index continuation monad
	- Can combine comp monads with different return types
