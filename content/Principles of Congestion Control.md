*Congestion* is when there are too many sources that are sending data too fast for the *network* to handle. 

It can lead to *long delays* and [[Packet Queuing and Loss]]. 

## Causes/Costs of Congestion 
### Scenario 1
![[Pasted image 20241204180639.png]]
In the scenario above, there are *delays* at $\lambda_{in} = \frac{R}{2}$ due to *queueing*.

### Scenario 2
![[Pasted image 20241204181953.png]]
![[Pasted image 20241204182000.png]]

### Scenario 3
![[Pasted image 20241204182147.png]]
![[Pasted image 20241204182154.png]]


![[Pasted image 20241204182202.png]]

## Approaches towards Congestion Control
### End-end Congestion Control
![[Pasted image 20241204182318.png]]
- no explicit feedback from network 
- congestion *inferred* from observed loss, delay 
- approach taken by classic TCP

### Network-assisted Congestion Control
![[Pasted image 20241204182406.png]]
- Routers provide *direct* feedback to sending and receiving hosts with flows passing through congested router
- may indicate congestion level or explicitly set sending rate 


