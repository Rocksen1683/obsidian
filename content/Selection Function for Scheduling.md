The *selection function* determines which processes among the ready processes is selected next for execution.

The *selection function* can be based on: 
- Priority 
- Resource Requirements 
- Execution Characteristics of the process 

In the case that it is based on the *execution characteristics*, then these quantities are useful: 
- $w$:  time spent in the system *waiting*
- $e$:  time spent in *execution* so far 
- $s$:  total *service time* required by the process including $e$
	- $s$ is usually estimated or supplied by the user 

