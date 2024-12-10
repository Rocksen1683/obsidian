Before exchanging data, the sender and receiver agree to establish a *connection* and agree on *connection parameters* (like starting sequence etc).

![[Pasted image 20241204175702.png]]

## 2-Way Handshake
![[Pasted image 20241204175836.png]]

![[Pasted image 20241204175843.png]]

**Happy Path:**
![[Pasted image 20241204175901.png]]

**Problem:**
![[Pasted image 20241204175919.png]]

## TCP's Solution 
To overcome the problems with the *2-Way Handshake*, TCP uses a *3-Way Handshake* which is necessary and sufficient for reliable startup and graceful shutdown. 

- `SYN`: used for *startup*
- `FIN`: used for *shutdown*

![[Pasted image 20241204180131.png]]

To close a [[Transmission Control Protocol]] connection, the client and server each close their side of the connection by sending a TCP segment with a `FIN` bit = 1. 

To respond to the received `FIN` with `ACK`, the `ACK` can be combined with the `FIN` on receive. 

`FIN` exchanges can be simultaneous. 
