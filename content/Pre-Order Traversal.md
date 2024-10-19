An *pre-order* [[DFS for Trees]] is a traversal where we go depth first but from top to bottom. That is root $\rightarrow$ leaf 

![[Pasted image 20240213150642.png]]

For the above example [[Binary Search Tree]], the *pre-order* traversal would be:
$$1 \rightarrow 2 \rightarrow 4 \rightarrow 5 \rightarrow 3$$
**Order of Traversal:** root $\rightarrow$ left $\rightarrow$ right
## Implementation 

```python 
def inOrder(node):
	#visiting the rnode 
	print(node.val)

	#visiting the left node
	if(node.left):
		inOrder(node.left)
	
	#visiting the right node 
	if(node.right):
		inOrder(node.right)

def DFS(root):
	inOrder(root)

```

**Time Complexity:** $O(n)$ as we visit every node once 
**Space Complexity:** $O(\log n)$ for  [[Binary Search Tree]]

## Iterative Solution 
``` python 
s = [] #stack 

def preOrder(node):
	current = node 

	while current or s :
		if currNode:
			print(current.val) #pre-order 
			s.append(current)
			current = current.left 

		else: 
			#reached end of left tree, go right of previous
			previous = s.pop() 
			current = previous.right 
			
```