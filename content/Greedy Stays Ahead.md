
$S$ is the *solution set* of the [[Greedy Algorithms]]. 
Assume $O$ is an optimal solution. Our goal is to **show** $|S| = |O|$. 
- Suppose $i_{1}, i_{2}, ..., i_{k}$ are the intervals in $S$ in the order they were added to $|S|$ by the greedy algorithm
- Similarly, let the intervals in $O$ are denoted by $j_{1}, ..., j_{m}$. Assume that intervals in $O$ are ordered in the order of the start and finish times. 
- We can do this by **proving** $k=m$

Before proving this we, need to prove and use a lemma 
### Lemma 
For all indices $r \leq k$
$$f(i_{r}) \leq f(j_{r})$$
where $f()$ is the *finishing time* of a particular algorithm. 

#### Proof:
We can use induction to prove this statement. 

**Base Case:**
The base case is $r=1$, and the statement is *true* for this case. 

**Inductive Step:**
Let us assume that the statement holds for $r-1$ where $r > 1$. 
Now using the inductive hypothesis, we would prove that the statement holds true for $r$

By the inductive hypothesis, we get, 
$$f(i_{r-1}) \leq f(j_{r-1})$$
Now, if we compare the *finish time* of $j_{r-1}$ and the *start time* of $j_r$, we get 
$$f(j_{r-1}) < s(j_{r})$$
Now using the above two equations, we get 
$$f(i_{r-1}) < s(j_{r})$$
At the time, the greedy algorithm had to choose the $r^{th}$ interval, the interval $j_r$ was a possible choice. The greedy algorithm chooses an interval with the smallest finish time. 
This means that the greedy algorithm will choose $i_r$.
So, 
$$f(i_{r)}\leq f(i_{r})$$

### Proof of |S| = |O|
To prove this statement, we can use contradiction. For the sake of contradiction, let us assume that 
$$|S| < |O|$$
This means that there exists element $j_{k+1}$ in $O$ as it has at least one more element in comparison to $S$. 

Now from the previous *Lemma*, we can say that 
$$f(i_{k}) \leq f(j_{k}) < s_{k+1}$$
So, the greedy algorithm could add $j_{k+1}$ to $s$, but it did not so we arrive at a contradiction that $|S|< |O|$. 


$$$$