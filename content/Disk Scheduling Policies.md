*Disk Scheduling Policies* are the order in which we pick processes from a queue that are requesting reads/writes from the disk. 

#### Random Scheduling 
- Randomly select the processes from the queue 
- Used as a *benchmark* but often gives poor performance. 
#### First in First Out 
- If process comes in quick -> goes out quick 🧠
- Pretty fair and super easy to implement and understand 
- Good performance when -> only few processes require access and if many requests are *clustered* into file sectors 
- Usually gives similar performance as *random scheduling* 😿
#### Priority Based 
- If we introduce priority, control of scheduling $\to$ outside of disk management
- Allows *short batch jobs* to be flushed quickly as they have higher priority 
- May cause *long term jobs* to *starve* 🥓
#### Shortest Service Time First (SSTF)
- Select the disk I/O request that requires the least movement of the disk arm from current position -> *choose minimum seek time*
- Provides better performance compared to FIFO
- In case of equal dist $\to$ random tie-breaking algo
- High utilization, small queues
#### SCAN (Elevator Algo)
- Prevents starvation by moving in one direction only until all outstanding requests en route are satisfied.
- SCAN behaves pretty much like SSTF
- Biased against area most recently traversed 
- Favors jobs which request tracks that are close to the innermost or outermost tracks and does not exploit locality like SSTF. 
#### C-SCAN
- Known as *Circular SCAN* and is like SCAN but restricts scan direction to one direction only 
- After it makes one rotation in one direction, it keeps going in the same direction 
- Solves the issue of *locality* that SCAN had 
#### N-STEP-SCAN  & FSCAN
- Segment the disk request queue in both of these 
- **N-Step SCAN:** segments the disk request queue into subqueues of length $N$. These subqueues are processed on at a time 
	- Large values of $N$ $\to$ performance of SCAN 
	- $N = 1$ $\to$ FIFO policy adopted
- **FSCAN:** segments disk request queue into $2$ subqueues
	- Scan begins $\to$ all requests are in one queue 
	- During scan $\to$ all new requests in other queue 
	- Service of new requests $\to$ deferred until all old requests are processed 

