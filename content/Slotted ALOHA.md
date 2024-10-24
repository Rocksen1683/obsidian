Allows collision to happen and then recover via retransmission and use *randomization* to recover from collisions. 

## Setup 
- All frames have the same size 
- Time is divided into equal time slots (time to transmit $1$ frame)
- nodes are synchronized 
- nodes begin transmissions at slot start times 
- if $2$ or more nodes transmit in the slot, the collision is detected by senders 


- When a node has a new frame to send, it transmits it in the next *time slot*. 
	- if *no collision*, then the node successfully transmits the frame 
	- if *collision*, node retransmits the frame in each subsequent slots with some probability $p$ until success. 

![[Pasted image 20241024150411.png]]

## Analysis 
### Pros 
- Single active node can continuously transmit at the full rate of the channel 
- Highly decentralized and only slots in the nodes need to be in sync 
- Simple

### Cons 
- synchronization required 
- collisions end up wasting slots 
- idle slots keep wasting slots 

## Efficiency 
The *efficiency* can be defined as the long-run fraction of successful slots (many nodes, all with many frames to send)

If we have $N$ nodes with multiple frames to send, each transmits in slot with probability $p$:
- prob that a given node has success in a slot would be $$p(1-p)^{N-1}$$
- prob that any node has a success: $$Np(1-p)^{N-1}$$
- max efficiency: find $p^{*}$ that maximizes $$Np(1-p)^{N-1}$$
- for many nodes, taking the limit of $$lim_{N \longrightarrow \infty}Np^{*}(1-p^{*})^{N-1}$$

we get, *max efficiency* is 
$$max_{e}= \frac{1}{e} = 0.37$$

This means that *at best*, the channel is used for useful transmissions only $37\%$ of time :( 