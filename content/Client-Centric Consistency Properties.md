### Monotonic Reads
If a client *reads* the value of $x$, later reads of $x$ by that same client will always return the same value or a more recently written value. 
![[Pasted image 20241208010507.png]]

### Read Your Writes
If a client *writes* a value to $x$, later reads of $x$ by that same client will always return the same value or a more recently written value.
![[Pasted image 20241208010520.png]]
### Monotonic Writes
If a client writes twice to $x$, the first write must happen before the second. 
![[Pasted image 20241208010532.png]]
