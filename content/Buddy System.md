The buddy system helps overcome some issues with [[Fixed Partitioning]] and [[Dynamic Partitioning]]

Every memory block would have some size $2^k$ such that 
$$2^{L} \leq 2^{k} \leq 2^{U}$$
where $L$ and $U$ are the *lower* and *upper* bounds respectively. 

- We start out with *one big block* of size $2^U$
- If a block is allocated in between $2^{U-1}$ and $2^U$
	- allocate the whole memory block $2^U$
- Else, split memory into *two blocks* of size $2^{U-1}$ (*buddies*)
- Also maintain a list of *holes* of size $2^{i}$

We can remove holes using the following algorithm 
```
void get_hole( int i) { 
	if (i == (U + 1)) <failure>; 
	if (i_list empty) { 
		get_hole(i + 1); 
		<split hole into buddies>; 
		<put buddies on i_list>; 
		} 
	<take first hole on i_list>; 
	}
```

![[Pasted image 20240309232013.png]]
