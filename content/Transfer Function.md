The *transfer function* of a system is the ratio of the Laplace transform of it's output and it's input, *assuming zero initial conditions.* 


$$G(s) = \frac{\mathcal{L}(y(t))}{\mathcal{L}(u(t))} = \frac{Y(s)}{U(s)}$$
where 
$$\dot{x} = Ax + Bu$$
$$y = Cx + Du$$
now when we take the *Laplace transform* of this will be 
$$sX(s) - x(0^{-}) = AX(s) + BU(s)$$
where $x(0^{-})$ will be 0 as we assume zero initial conditions. 
$$Y(s) = CX(s) + DU(s)$$
$$sIX(s) - AX(s) = BU(s)$$
where $I$ is the *identity matrix*
$$(sI - A)X(s) = BU(s)$$
$$\implies X(s) = (sI - A)^{-1}BU(s)$$
Now we know that we can't get an *inverse* of a matrix when the *determinant* is zero. 
We know that the determinant will be zero when 
$$det(sI - A) = 0 \implies s \in eig(A)$$
Now that we have a value for $X(s)$, let us substitute it in the $Y(s)$ equation, giving
$$Y(s) = C(sI - A)^{-1}BU(s) + DU(s)$$
p
$$Y(s) = G(s)U(s)$$
where $G(s)$ is the *transfer function*

now this will have a matrix dimension of $R^{p\times m}$ where $Y(s) \in R^p$ and $U(s) \in R^m$
What this means is that $G_{ij}$ represents the *influence* of $U_{j}(s)$ on $Y_i(s)$ 

Now if you notice the final equation, you can see that we have no information of the state of the system $x$ or $X(s)$. This means that our initial system has 

### Definitions

- [[Real Rational TF]]
- [[Poles and Zeros]]


### [[Transfer Function Examples]]