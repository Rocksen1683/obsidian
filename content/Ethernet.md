## Topology 
- *bus*: all nodes in same collision domain (can collide with each other)
- *switched*: prevails today and has an active link layer 2 *switch in the center*


## Frame Structure 
![[Pasted image 20241025001942.png]]
![[Pasted image 20241025002003.png]]

## Problems 
Ethernet is usually *unreliable* (receiver doesn't send ACKs or NAKs to sender; data in dropped frames are hard to recover) and *connectionless* (no handshaking between sender and receiver).

Ethernet uses *unslotted* [[CSMA-CD]] with *binary backoff* as it's [[Multiple Access Protocols]]
