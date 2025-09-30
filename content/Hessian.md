Let $f(v): R^{d} \longrightarrow R$ be a scalar valued function of $d$ variables. 

The ***hessian*** is defined as
$$\nabla ^{2}f(v): R^{d} \longrightarrow R^{d\times d}$$
which would look like 

![[Pasted image 20250909140959.png]]

So the resultant matrix would have a dimensionality of $d \times d$
### Example

$$f(v) = 2v_{1} + v_{2}^{2}$$
$$\nabla f(v) = \left(  \frac{\partial f}{\partial v_{1}},\frac{\partial f}{\partial v_{2}} \right)$$
$$ = (2v_{2}, 2v_{1} + 2v_{2})$$
$$\nabla ^{2}f(v) = \begin{bmatrix} 0 & 2 \\
2 & 2 \end{bmatrix}$$
