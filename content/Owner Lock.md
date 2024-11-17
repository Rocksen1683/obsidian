![[Pasted image 20241031125944.png]]
- `owner()` returns nullptr if no owner, otherwise address of task that currently owns lock. 
- `times()` returns number of times lock has been acquired by owner task.
- Must release as many times as acquire.
- Otherwise, operations same as for uLock but with blocking instead of spinning for acquire