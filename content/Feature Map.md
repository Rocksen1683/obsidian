A *feature map* $\phi$ maps a feature vector $x$ to some higher-dimensional space. 

An example would be the *padding trick* which would map 
$$\phi(x) = [x, 1]$$
and parameter vector 
$$w = [p, b]$$
which would be both $R^{d+1}$

### Quadratic Feature Maps
Instead of functions $x^{T}p + b > 0$, consider 
$$x^{T}Qx+ \sqrt{2}x^{T}p+ b > 0$$

where 
- $Q \in R^{d\times d}$
- $p \in R^{d}$
- $b \in R$

**Note:** 
$$x^{TQx}= \sum\limits (x_{i}x_{j}Q_{ij})$$


For the circle case described in [[Kernels]], the $Q$ matrix would look like
$$Q = \begin{bmatrix} 1 & 0 \\ 0 & 1\end{bmatrix}$$

We know that the dot product between the *flattenings* of $xx^T$ would look like 
$$xx^{T}= \begin{bmatrix} x_{1}x_{1} & x_{1}x_{2} & ... \\ \\
x_{2}x_{1} & ... \\ \\
... \\
\\& & x_{2}x_{2} \end{bmatrix} \in R^{d \times d}$$

Now, we can flatten this by making this into a vector in $R^{d^{2}}$
$$\vec{xx^{T}}= \begin{bmatrix} x_{1}x_{1} \\x_{1}x_{2} \\ ... \\ x_{2}x_{2}
\end{bmatrix} \in R^{d^{2}}$$
this makes it easier.
$$\vec{Q} = \begin{bmatrix} Q_{11} \\ Q_{12} \\ ... \\ Q_{22}
\end{bmatrix} \in R^{d^{2}}$$




Now, we can take 
$$\phi(x) = [\vec{xx^{T}}, \sqrt2 x, 1]$$
and
$$w = [\vec{Q}, p, b]$$
both in $R^{d^{2} + d + 1}$


Then 
$$<\phi(x), w> \longleftrightarrow x^{T}Qx + \sqrt{2}x^{T}p + b$$
However, with this [[Quadratic Feature Maps]], we see that computations go from $R^{d}\longrightarrow R^{d^{2} + d + 1}$
which means the runtime goes from $O(d) \longrightarrow O(d^{2})$.


With this we can see that, if we map to a very high dimensional space, our runtime will also go really high. 

