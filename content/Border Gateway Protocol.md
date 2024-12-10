*BGP* is the *inter-domain* routing protocol and is the glue that holds the internet together. 

### eBGP
Obtain destination network reachability info from neighbouring AS's 

Runs between two routers that belong to *different* autonomous systems
### iBGP
Propagate reachability information to all AS-internal routers

Runs between two routers that belong to the *same* autonomous systems

*Gateway Routers* run both *eBGP* and *iBGP* protocols.

![[Pasted image 20241203184036.png]]

![[Pasted image 20241203184049.png]]

### BGP Path Advertisement
![[Pasted image 20241203184109.png]]
![[Pasted image 20241203184131.png]]

### BGP Messages
*BGP Messages* are exchanged between peers over the TCP connection. 

![[Pasted image 20241203184234.png]]

### Hot potato Routing
![[Pasted image 20241203184526.png]]

Choose a local gateway that has the least *intra-domain* cost 

