For *linear regression*, the loss function $l_w$ is :
$$\sum\limits (y_{i}- <w, x_{i}>)^2$$
The resulting *predictor* is 
$$y = <w, x>$$
This is a *linear model* and would not be optimal when the *line of best fit* is a polynomial. 

### Loss Function

Let $A \in R^{n \times d}$  be the *feature vectors* and $z \in R^{n}$ be the *labels* in vector form. 
$$A = \begin{bmatrix} x_{1}... \\
... \\
x_{n} ...\end{bmatrix}$$
$$z = \begin{bmatrix} y_{1} \\
... \\
y_{n}\end{bmatrix}$$
$$Aw - z = \begin{bmatrix} <w, x_{1}> - y_{1}\\
... \\
<w, x_{n}> - y_{n}\end{bmatrix}$$
$$$$
The linear regression *loss function* is equivalently
$$||Aw - z||^{2}_{2}$$
The [[Euclidean Norm]] squared of $Aw - z$ would be 
$$\sum\limits(<w, x_{i}> - y_{i})^{2}$$

### Loss Function Convexity

The loss function $l_{w}$ which is $||Aw - z||^{2}_{2}$ can be written as 
$$||Aw - z||^{2}_{2} = (Aw - z)^{T}(Aw- z) = (w^{T}A^{T}- z^{T})(Aw-z)$$
$$= w^{T}A^{T}Aw - z^{T}Aw - w^{T}A^{T}z + z^{T}z$$
$$= w^{T}A^{T}Aw - 2w^{T}A^{T}z + z^{T}z$$
**Note**: $z^{T}Aw$  and $w^{T}A^{T}z$ are *scalar* values and can be grouped together as their transpose will be the same. 

**Claim:** If $f(x) = x^{T}Ax + x^{T}b + c$, then $\nabla f(x) = (A + A^{T})x + b$

Thus 
$$\nabla _{w}||Aw - z||^{2}_{2} = 2A^{T}Aw - 2A^{T}z$$

Now if we look at the [[Hessian]], which is 
$$\nabla ^{2}_{w}||Aw - z||^{2}_{2} = 2A^{T}A \succeq 0$$
![[Pasted image 20250911135112.png]]

This proves that the linear regression *loss function* has the property of [[Convexity]].

### Optimizing Least Squares

As we know that our *loss function* is *convex*, we can set the gradient to 0 which minimize the function. 

![[Pasted image 20250911135826.png]]


- [[Maximum Likelihood Principle]]

### [[Hyperparameter Selection]]
