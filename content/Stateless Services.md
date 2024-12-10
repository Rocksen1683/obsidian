A *stateless* thread/service remembers nothing from past requests and has no *local* state. 

A *stateful* thread changes over time as a side effect of handling requests and uses persistent global variables. 

The reason a *stateless* service is better as it's better for [[Horizontal Scaling]] due to the fact that we don't store previous data and it does not matter which copy processes a particular request. 

*SMTP* in the [[Application Layer]] is a *stateful* protocol whereas *HTTP* is a *stateless* protocol. 

[[Cookies]] are how *web applications* main statelessness while still remembering some information. 

### How does statelessness help?
![[Pasted image 20241207213912.png]]
