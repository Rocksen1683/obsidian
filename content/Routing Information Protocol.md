*RIP* is used as a *intra-AS* [[Routing Protocols]] that uses the [[Distance Vector Algorithm]] every 30 seconds. It's not widely used anymore

![[Pasted image 20241203174713.png]]

### Failure and Recovery 
If no advertisement is heard after 180 seconds, then the neighbour link will be declared *dead*. 
![[Pasted image 20241203174800.png]]

### Problems 
- Convergence is slow 
- Loops can be formed due to routing table inconsistency which would lead to [[Packet Queuing and Loss]]. 
- Loops could last a long long time 
