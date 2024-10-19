## Problem 

![[Pasted image 20240213134637.png]]

Total completion time will mean adding the sum of predecessors while calculating current. TCL for the above example is $70$.
## Algorithm 
Order the job in an *increasing*/*non-decreasing* order. 

### Run-time 
Run-time of the algorithm would be synonymous to sorting $\implies O(n \log n)$

### Proof of Correctness 
To prove this, we can use something called an [[Exchange Argument]]

Assume that there is an optimal solution with a different ordering in comparison to the solution given by the greedy algorithm. 

Suppose $L = [e_{1}, .., e_{n}]$ is an optimal solution and $L$ is not in a *non-decreasing* order of processing times. 

Now as $L$ definitely has a different ordering from our greedy algorithm, we can say that:
There exists an index $i$ such that $t(e_{i}) > t(e_{i+1})$

We know that the sum of completion times of $L$ is 
$$nt(e_{1}) + (n-1)t(e_{2}) + ... + t(e_{n})$$
The contribution of $e_i$ and $e_{i+1}$ is:
$$(n - i +1)t(e_{i}) + (n-i)t(e_{i+1})$$
Now, *switch* $e_{i}$ and $e_{i+1}$ to get a new permutation $L'$. Their contribution becomes:
$$(n - i +1)t(e_{i+1}) + (n-i)t(e_{i})$$
Nothing else changes so we can say that 
$$T(L') - T(L) = t(e_{i+1} - t(e_{i})) < 0$$
Which means that they are not the ***same***, leading to a *contradiction* to our assumption. Hence our initial assumption was wrong and we would need a *non-decreasing* order of processing times to get an optimal solution for the problem. 