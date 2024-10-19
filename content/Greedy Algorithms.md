## Problem 
The problem that *Greedy Algorithms* solve is that of **combinatorial optimization** that
- have a *large*, but *finite* domain $D$ 
- want to find an element $E$ in $D$ that *minimizes/maximizes* a cost function
### Greedy Strategy
The greedy algorithm strategy involves
- building $E$ step-by-step
- improving as much as you can at every step 
- simple algos but no guarantee to get optimal solution 
- hard to prove correctness, easy to prove incorrectness 
-

#### Greedy strategy as Pseudocode 

	
	```pseudocode
	Algorithm Greedy(A, n):
		for i = 1 to n:
			x = select(A)	
			if x is feasible then: 
				solution = solution + x```
				

### [[Greedy Correctness Proofs]]

## Problems 
- [[Fractional Knapsack Problem]]
- [[Interval Scheduling]]
- [[Interval Coloring]]
- [[Minimizing Total Completion Time]]
