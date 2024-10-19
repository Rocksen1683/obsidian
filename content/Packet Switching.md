Hosts break down application-layer messages into *packets*. 

The network *forwards* these packets from one router to another, across links on a path. 

## Switching at the Source
- Host takes application message 
- Breaks it into smaller chunks, called *packets* (each with length $L$ bits)
- Transmits packets into access network at some *transmission rate* $R$, aka link capacity

![[../Pasted image 20241019133445.png]]
### Transmission on each link 
![[../Pasted image 20241019133751.png]]

For the packet to fully reach the receiver, the total amount of time would be:
$$\frac{L}{R} + prop\_delay$$
### Store and Forward
*Entire* packet must arrive at the router before it can be transmitted to the next link. The router stores the packet chunks until the whole packet fully arrives. 

![[../Pasted image 20241019134126.png]]

The *pipelining effect*: packets shouldn't be too big, better break up a big file into smaller ones. 

## Buffers and Queuing
*Buffers* are needed for storing, processing, and forwarding within [[Packet Switching]]. 
Would need some smart scheduling and discarding policies for the buffer. 

Multiple packets share resources (buffers, links) without reservation. 

*Queuing* occurs when work arrives faster than it can be serviced. 

### [[Packet Queuing and Loss]]