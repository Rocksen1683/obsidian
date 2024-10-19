Partitions are of *variable* length and number. Memory is allocated based on how much a process requires. 

![[Pasted image 20240309225142.png]]

This *starts* out well but as we keep adding and deleting processes, we ill end up having ***holes*** in memory which is called ***External Fragmentation***. 

One way to overcome *external fragmentation* would be to use a technique called ***compaction*** which would move all of the *fragments* of free space together to create one big block. Issue with this would be that it is a *time-consuming* process and would waste processor time. 

### Placement Algorithm
Here are some placement algorithms used for dynamic partitioning, *best-to-worst*
- **First Fit:** fits the block into the first free block that would satisfy the requirement 
- **Next Fit:** fits the block into the next free block (that would satisfy) from current block 
	- would use *compaction* a lot as the next block usually be the big chunk in the end which creates a lot of fragments
- **Best Fit:** fits the block into the block with the closest amount of size allocated 
	- Very *inefficient* as we would keep iterating to find the best fit but would also have fragments 

