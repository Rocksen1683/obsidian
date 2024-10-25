An *ethernet switch* is a [[Link Layer]] device that stores and forwards [[Ethernet]] frames. It examines the incoming frame's [[MAC Address]] and *selectively* forwards the frame to one or more outgoing links and uses [[CSMA-CD]] to access each link as it's [[Multiple Access Protocols]].

They are also *unaware* of the presence of other switches and do not need to be configured. 

## Multiple Simultaneous Transmissions 

![[Pasted image 20241025002646.png]]

## Switch Forwarding Table
![[Pasted image 20241025002705.png]]
In the above diagram, the *switch* knows that $A'$ is reachable by interface $4$ as each switch has a ***switch table*** where each entry has:
- [[MAC Address]] of the host
- Interface to reach the host 
- Timestamps 

The switch *learns* which hosts can be reached through which interfaces as when a frame is received, the switch *learns* the location of the sender and the incoming LAN Segment. This allows it to populate the switch forwarding table with the appropriate information. 
## Interconnecting Switches 
These *self-learning* switches can be connected together to form *interconnecting switches*. 

## [[Switches vs Routers]]