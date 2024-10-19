## Problem 

![[Pasted image 20240213133328.png]]

## Algorithm 
- Sort the intervals by starting time: $s_{1} \leq s_{2} \leq ... \leq s_{n}$
- For $i$ from $1$ to $n$ do:
	- Use minimum available color $c_i$ to color the interval $i$ so that it doesn't conflict with the colors of the intervals that are already colored 

### Run-time 
The run-time of this algorithm would be $O(n^2)$. 
We can make it more efficient by using a ***Min-Heap*** which would get it down to $O(n \log n)$

### Proof of Correctness 
If the greedy algorithm uses $k$ colors, then $k$ is the minimum number of colors needed. In other words, no other algorithm can solve the problem with $k-1$ colors. 

**Idea**: Show that there exists a time $t$ such that it is contained in $k$ intervals. 

Assume $l$ is the first interval which uses the color $k$.
Since we have increasing order of start times that is $s_{i_{j}} \leq s_{l}$, , $1 \leq j \leq k-1$. 
On the other hand, all the intervals overlap with $[s_{l}, f_{l}]$, hence, 
$$s_{l}\leq f_{i_{j}}$$
Hence $s_{l}$ is a time contained in $k$ intervals which proves that there is **no** $k-1$ coloring. 
