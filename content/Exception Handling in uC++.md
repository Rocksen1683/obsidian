In `uC++`, you declare an exception by `_Exception`.
```
_Exception exception-type-name { ... };
```

### Raising an Exception 
- `_Throw` has no exception-type, it is a rethrow 
- `_Resume` has no exception-type, it is a reresume 
- NEVER THROW `_At` as it allows the specified exception or currently propogating exception to be raised by another coroutine 

### Exception Handlers 
For a `_Throw`: just use a `catch`. 
For a `_Resume`: you would need to use `_CatchResume`.

NOTE: Always put a `_CatchResume` *before* a `catch`

*Resumption Handler* cannot perform a break, continue, goto, or return. 
