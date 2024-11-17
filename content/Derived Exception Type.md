*Derived Exception Types* is a mechanism for inheritance of exception types, like inheritance of classes. 

![[Pasted image 20241030174258.png]]

Higher-level code should catch general exception-types to reduce tight coupling to the specific implementation.

```
try { . . . } 
catch( Arithmetic & ) { . . . } 
catch( Overflow ) { . . . // never selected!!! }
```

It is a good idea to catch an exception *by reference* as it would *truncate* otherwise from it's dynamic type to static type specified at the handler.

