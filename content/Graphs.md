## Implementation
```python
#importing defaultdict so that we get a dictionary of lists 
from collections import defaultdict

class Graph: 
	def __init__(self):
		self.graph = defaultdict(list) #creates a dict with list as values

	def add_edge(self, u, v):
		self.graph[u].append(v)
	
```

## Main Topics 
[[DFS for Graphs]]
[[BFS for Graphs]]
[[Union Find]]
[[Topological Sort]]

## Questions 
[[207. Course Schedule]]
[[133. Clone Graph]]
