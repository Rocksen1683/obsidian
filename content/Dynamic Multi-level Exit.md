Rather than returning one level at a time, simpler for new modularized routine to bypass intermediate steps and transfer directly to original caller.

Extend call/return semantics to transfer in the reverse direction to normal routine calls, requiring nonlocal transfer.

![[Pasted image 20241030111433.png]]

### [[Label]]
### [[goto]]

In *C*, we use the following for [[Dynamic Multi-level Exit]]
- `jmp_buf`: to declare label variable 
- `setjmp`: to initialize label 
- `longjmp`: to goto label variable 

![[Pasted image 20241030112401.png]]
