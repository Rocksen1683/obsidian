## Iterative 
Data Structures used: **Queue** and **Hash Set**
Here's how we use them: 
- **Queue**: To keep track of the order of traversal
- **Hash Set**: To keep track of the nodes we have visited 
### Implementation 
```python
def bfs(G, s):
	#G is a graph, s is the source vertex 
	queue = [] #queue data structure
	visited = set() #hash set data structure 

	queue.append(s) #addingf first element to queue

	while queue:
		v = queue.pop(0) #popping vertex 
		print(v) #searched v 

		#iterating through neighbours of vertex v 
		for i in G[v]:
			if i not in visited:
				visited.add(i) #to ensure that we don't visit vertex again 
				queue.append(i) #adding to queue to explore i's neightbors 
```
