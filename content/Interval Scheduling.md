## Problem Definition 
#### Input 
- $s:$ array of *start times* of an interval 
- $f:$ array of *finish times* of an interval 
#### Output 
Return the maximum number of *disjoint* intervals

### Proof of Correctness: 
To prove the *correctness* of this algorithm we would have to 
- Prove by contradiction that there doesn't exist an *optimal solution* $O$ such that $|S| < |O|$ where $S$ is the *greedy solution*
- 