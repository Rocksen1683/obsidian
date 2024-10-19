The breadth-first exploration of  [[Undirected Graph]] can be done in the following way. 

![[Pasted image 20240125130837.png]]

## Complexity 
### Analysis 
- each vertex is enqueued at most once 
- each vertex id dequeued at most once 
- each adjacency list is read at most once 
For all $v$, write $d_v$ as the number of neighbors 

**Total Run-time:** $O(n + m)$ where $n$ is number of vertices and $m$ is number of edges
## Correctness 
To prove the correctness of [[Breadth First Search for Undirected Graph]], let us prove and use the following lemmas

### Lemma 1
#### Claim 
For all vertices $v$, if visited$[v]$, is True at the end, there is a path $s \rightarrow v$ in $G$. 
#### Proof 
Let $s=v_0...v_k$ be vertices for which visited is set to true, in this order. We prove for **all $i$, there is a path $s \rightarrow v_i$** by induction

**Base case:** This would work for $i=0$ as $v_{0}\rightsquigarrow v_{0}$ is a valid path. 
**Inductive Step:** 
Let us assume that for the sake of induction, that the statement holds true for some vertex $v_k$. This means that there is a path $s \rightsquigarrow v_k$ . 

Now for a vertex $v_{k+1}$, if visited$[v_{k+1}]$ is *true*, and we know that ${v_{k,}v_{k+1}} \in E$, so there is a path $s \rightsquigarrow v_{k+1}$
#### Claim 
For all vertices $v$, if there is a path $s \rightarrow v$ in $G$, visited$[v]$  
is true at the end. 
#### Proof 
Let $v_0 = s, . . . , v_k = v$ be a path $s \rightarrow v$. We prove  
visited$[v_i]$ is true for all $i$, by induction.  

**Base Case:** visited$[v_{0}]$ is true  

**Inductive Step:**  Assuming visited$[v_i]$ is true, we will examine all neighbors $u$ of $v_i$  
At the end of Step 7 (in the pseudocode), all visited$[u]$ will be true, for $u$ neighbor of $v_i$.
We know that $v_{i+1}$ would be a neighbor $v_{i}$ as it would be in the 
This would mean visited$[v_{i+1}]$ will be true . 

## BFS Lemma 
For all vertices $v$, there is a path $s \rightarrow v$ in $G$ **if and only if** visited$[v]$ is True at the end. 
### Applications of the lemma 
- Testing if there is a path $s \rightarrow v$
- Testing if $G$ is connected 
### Run-time of the Lemma 
Run-time of the lemma would be $O(n+m)$

## Keeping track of parents/predecessor and levels

![[Pasted image 20240125132737.png]]


[[BFS Tree for Undirected Graphs]]
[[BFS to Test Bipartiteness]]
[[Computing Connected Components]]