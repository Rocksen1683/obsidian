*Queues* are typically described using Kendall Notation of the form A/S/C/B/K/D where:
- **A** corresponds to the *arrival process* of the packets (more precisely the distribution of the inter-arrival time between packets). A can be M (Markovian or Exponential), D (Deterministic) or G (General).
- **S** corresponds to the *server process* for the packets. S can again be M, D or G.
- **C** corresponds to the *number of servers* (or network interfaces). 
- **B** corresponds to the *buffer size*, i.e. the number of packets that can be accommodated in the “waiting room”. If  omitted, the buffer is assumed to be infinitely large
- **K**: corresponds to the *population size*
- **D** corresponds to the *queuing discipline* which is almost always FIFO 
### Example
![[Pasted image 20241209211459.png]]
