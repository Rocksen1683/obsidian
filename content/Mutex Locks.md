*Mutex Lock* is used solely to provide mutual exclusion. 

Two kinds:
1. *Single Acquisition*: task that acquired the lock cannot acquire it again
2. *Multiple Acquisition*: lock owner can acquire it multiple times, called an [[Owner Lock]]

## Implementation
![[Pasted image 20241031125713.png]]
![[Pasted image 20241031125719.png]]

### Barging Avoidance
Hold avail between releasing and unblocking task (bounded overtaking). (see [[Bounded vs Unbounded Overtaking]])

![[Pasted image 20241031125805.png]]
Bargers enter mutual-exclusion protocol but block so released task does not busy wait (if rather than while).

### Barging Prevention
hold lock between releasing and unblocking task (unbounded overtaking). (see [[Bounded vs Unbounded Overtaking]])

![[Pasted image 20241031125918.png]]
![[Pasted image 20241031125924.png]]
