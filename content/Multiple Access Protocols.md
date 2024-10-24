Distributed algorithm that determines how nodes share a channel and also determine when nodes can transmit. 

An ideal [[Multiple Access Protocols]] should when given a multiple access channel (MAC) of rate $R$ bps, ensure that:
1. When one node wants to transmit, it can send at a rate of $R$
2. when $M$ nodes want to transmit, each can send at an average rate of $\frac{R}{M}$
3. Fully decentralized: 
	- no special node to coordinate transmissions 
	- no synchronization of clocks, locks etc. 

## Types of Protocols
1. *taking-turns*: nodes take turns but nodes with more to send can take longer turns (uses *polling*)
2. *random access*: the channel is not divided and does allow collisions but is possible to "recover" from collisions
3. *channel partitioning:* divide the channel into smaller pieces based on time slots, frequency etc. Allocate piece to node for exclusive use. 

### [[Channel Partitioning MAC Protocol]]

### [[Random Access Protocols]]