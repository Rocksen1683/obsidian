Allows [[Routines]] to transfer back to its caller but not after the call. 

## Approaches 
Following are approaches to handle multiple-outcomes. 

- *return code*: returns value indicating normal or exceptional execution. ex: `printf()` returns number of bytes transmitted or returns negative val when fails 
- *status flag*: use a flag for status of program 
- *fix-up routine*: global/local routine called for exceptional event to fix up and return a corrective result. 
- *return union*: combines returning code and requiring return-code check on result access.


## [[Dynamic Multi-level Exit]]
## [[Exception Handling in uC++]]