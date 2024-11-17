A *coroutine* is a routine that can also be suspended at some point and resumed from that point when control returns. 

The state of a *coroutine* consists of:
- *execution location*: starting at the beginning of the coroutine and remembered at each suspend 
- *execution state*: holding the data created by code the coroutine is executing $\implies$ each coroutine has it's own stack 
- *execution status*

A coroutine does not start from the beginning on each activation; it is activated at the point of last suspension

[[Routines]] always start execution at the beginning and it's local variables persist for a single activation. 

![[Pasted image 20241030135211.png]]

## Types 
1. [[Semi-Coroutine]]
2. [[Full-Coroutine]]

## Coroutine Construction 
- Fibonacci consumes nothing and produces (generates) Fibonacci numbers ⇒ convert writes (cout) to suspends. 
- Formatter consumes characters and only indirectly produces output (as side-effect) ⇒ convert reads (cin) to suspends.

## Coroutine Implementations 
Coroutine implementations usually have two forms:
1. *stackless*: use the caller's stack and a fixed-sized local-state
2. *stackful*: separate stack and a fixed-sized (class) local state
### Python 
Stackless, semi coroutines, routine versus class, no calls, single interface

### JavaScript
Similar to Python: stackless, semi coroutines, routine versus class, no calls, single interface. Embedded in HTML with I/O from web browser.


### C++
`C++20` has an API for coroutines and outline code to build stackless, stackful, or even fibres. This capability cannot be used directly. It requires writing significant low-level implementation code.