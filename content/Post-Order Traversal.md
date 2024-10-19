An *post-order* [[DFS for Trees]] is a traversal where we go depth first but from bottom to up but we visit each child before going to root. That is leaf $\rightarrow$ root. This means that it is the *bottom-up* version of [[BFS for Trees]].

![[Pasted image 20240213150642.png]]

For the above example [[Binary Search Tree]], the *post-order* traversal would be:
$$4 \rightarrow 5 \rightarrow 2 \rightarrow 3 \rightarrow 1$$
**Order of Traversal:** left $\rightarrow$ right $\rightarrow$ root
## Implementation 

```python 
def inOrder(node):
	#visiting the left node
	if(node.left):
		inOrder(node.left)
	
	#visiting the right node 
	if(node.right):
		inOrder(node.right)

	#visiting the rnode 
	print(node.val)

def DFS(root):
	inOrder(root)

```

**Time Complexity:** $O(n)$ as we visit every node once 
**Space Complexity:** $O(\log n)$ for  [[Binary Search Tree]]

## Iterative Implementation 

``` python 
s = []
rightStack = [] #stack to hold right children 

def postOrder(node):
	current = node
	while s or current: 
		if current:
			if current.right:
				#push right child
				rightStack.append(current.right)
			#traversing through current 
			s.append(current)
			current = current.left 

		else: 
			current = s.pop()
			if rightStack and current.right = rightStack[-1]:
				current = rightStack.pop()
			else: 
				print(current.val)
				s.pop()
				current = None
```

