*Queues* are typically described using Kendall Notation of the form A/S/C/K/D where:
- **A** corresponds to the *arrival process* of the packets (more precisely the distribution of the inter-arrival time between packets). A can be M (Markovian), D (Deterministic) or G (General).
- **S** corresponds to the *server process* for the packets. S can again be M, D or G.
- **C** corresponds to the *number of servers* (or network interfaces). 
- **K** corresponds to the *buffer size*, i.e. the number of packets that can be accommodated in the “waiting room”. If  omitted, the buffer is assumed to be infinitely large
- **D** corresponds to the *queuing discipline* which is almost always FIFO 