Algorithm to find a [[Minimum Spanning Trees]] given a *weighted graph*. 

### Approach
- Start with the *minimum cost* edge from the graph 
- At that vertex, choose the next vertex as the minimum edge between all the *connected vertices* 
- Add the minimum vertex and repeat until end

### Pseudocode
```
V = set of vertices in G 
U = visited vertices = null 
T = visited edges = null 
V - U = not visited vertices
U = min(v in V)

while V - U is not null: 
	let (u, v) be lowest cost edge such that u in U and v in V - U
	T = T U {(u, v)}
	U = U U {v}

return U, T
```
