Acts symmetrically, like recursive routines, by explicitly activating a member of another coroutine, which directly or indirectly reactivates the original coroutine (activation cycle).

![[Pasted image 20241030165336.png]]

There are $3$ phases to any full coroutine:
1. Starting the cycle 
2. Executing the cycle 
3. Stopping the cycle 

