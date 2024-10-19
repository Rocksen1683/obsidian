### 1. Precomputation
The ranking vector $p^{\infty}$ cam be *precomputed* once and stored. 

### 2. Sparsity
In [[NLA - Numerical Linear Algebra]], we often deal with two kinds of matrices. 
- **Dense:** Most or all entries are *non-zero*. Store in an $N \times N$ array 
- **Sparse:** Most entries are *zero*. Use a *sparse* data structure to save space and time 

[[Sparse Matrix-Vector Multiplication]]

### 3. Exploiting Sparsity 
In the case that our matrix $M$ is *dense*, we can do the following manipulation. 

We can use [[NLA - Numerical Linear Algebra]] manipulations to perform 
$$p^{n+1}= Mp^{n}$$
without creating or storing $M$

Derivation Here: [[Exploiting Sparsity for Page Rank]]

## Algorithm
![[Pasted image 20240320132934.png]]
