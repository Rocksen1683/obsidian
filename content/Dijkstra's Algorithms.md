## Single-Source Shortest Path 
### Problem 
**Input:** $G = (V, E), w: E \rightarrow R$ where $w$ is the weight and a source 
$s \in V$
**Output:** A shortest path from $s$ to each $v \in V$

## Dijkstra's Algorithm

Dijkstra's Algorithm is a [[Greedy Algorithms]]

**Input:** A weighted [[Directed Graph]] with non-negative edge weights 

For all vertices, maintain quantities: 
- $d[v]$: a shortest-path estimate from $s$ to $v$ (representative of distance)
- $\pi[v]$: predecessor in the path (a vertex or $NIL$ 
### Approach  
Initialize $C = \phi$ and do the following until $C = V$
- Add $u \in V - C$ with *smallest* $d$ value to $C$
- Update $d$ values of vertices $v$ with $(u, v) \in E$
	- $d[v] = min\{d[v], d[u], + w(u, v)\}$
- Update $\pi [v]$ if $d[v]$ is changed 

For the vertices, we will use  [[Heaps]] (especially a *min-heap*)
![[Pasted image 20240229153028.png]]

### Relaxation of Vertices 
*Relaxation of vertices* in [[Dijkstra's Algorithms]] is defined as when we update the *distance* $d[v]$ of a vertex $v$. This is done by: 
```
if d[u] + w(u, v) < d[v]:
	d[v] = d[u] + w(u, v)
```

### Pseudocode 
![[Pasted image 20240229153122.png]]

### Run-time Analysis 
#### Array Implementation
The run-time using arrays to store vertices would be $O(|V|^2)$
#### Heap Implementation 
The run-time using heaps to store vertices would be $O((|V|+|E|)\log |V|)$

### Proof of Correctness 
#### Claim 
For each vertex $v \in V$, we have $d[v] = \delta(s, v)$ at the time when $v$ is added to set $C$. To prove, we follow the following steps 

1. **Proof by Contradiction:** Assume the claim is *not correct* and $u \in V$ is the first vertex for which $d[u] \neq \delta(s, u)$ when it is added to $C$
2. Time $t$: 


### Disadvantages of Dijkstra's 
The input to *Dijkstra's algorithm* is weighted graph that only allows ***positive weights***. Dijkstra's won't always work for negative edges as the relaxation condition of 
$$d[u] + w(u, v) < d[v]$$
would not necessarily work. 