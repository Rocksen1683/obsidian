An *eigenvalue* $\lambda$ and corresponding *eigenvector* $x$ of a matrix $Q$ are a non-zero scalar and vector which satisfy 
$$Qx = \lambda Ix$$
Rearranging this gives us 

$$(\lambda I - Q)x = 0$$

To find the *eigenvalues* $\lambda$ of $Q$, we need to solve the *characteristic polynomial* 
$$det(\lambda I - Q) = 0$$

### Example 
Find *eigenvalues*/*eigenvectors* for 
$$Q = \begin{bmatrix} 2 & 2 \\ 5 & -1\end{bmatrix}$$
To find them, solve 
$$det(\lambda I - Q) = 0$$
for $\lambda$ which gives us 
$$ det(\begin{bmatrix} \lambda - 2 & -2 \\ -5 & \lambda + 1\end{bmatrix}) = (\lambda - 2)(\lambda + 5) - (-2)(-5)$$
$$ = \lambda^{2}- \lambda - 12 = 0$$
Factor this as 
$$(\lambda - 4)(\lambda + 3) = 0$$
which give sus the roots as $\lambda_{1} = 4, \lambda_{2} = - 3$

Now, to find the eigenvectors, plug $\lambda$ back in $Qx = \lambda x$
$$\begin{bmatrix} 2 & 2 \\ 5 & -1\end{bmatrix}\begin{bmatrix} x_{1} \\ x_{2}  \end{bmatrix} = \begin{bmatrix} 4x_{1} \\ 4x_{2}\end{bmatrix}$$
First row say $2x_{1}+ 2x_{2}= 4x_{1}$ or $x_{1}= x_{2}$

So, any vector 
$$\vec{u}_{1} = c_1\begin{bmatrix} 1\\ 1\end{bmatrix}$$
for some arbitrary non-zero scalar $c$ is an eigenvector for $\lambda_{1} = 4$

Similarly for the other eigenvector, we get 
$$\vec{u}_{2}= c_{2}\begin{bmatrix} 2  \\ -5 \end{bmatrix}$$
