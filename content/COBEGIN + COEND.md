To create [[Threads]] with `COBEGIN` and `COEND`, we would:

![[Pasted image 20241001132607.png]]

It's *implicit* concurrency but not *explicit* concurrency. 
(See [[Implicit vs Explicit Concurrency]])

![[Pasted image 20241001132906.png]]


To create a dynamic number of threads with [[COBEGIN + COEND]], we would have to use *recursion*.

![[Pasted image 20241001133129.png]]
