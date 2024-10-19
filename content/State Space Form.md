The *state* of a system is a collection of variables which describes the evolution of the system until the current time. 

#### More useful definition 
The *state* $x(t)$ of a system is a collection of variables such that if we know $x(t)$ and the input signal to the system $u(t) \in [t_{0}, t_{1}]$, then we can compute $x(t_{1}), y(t_{1})$ where $y(t)$ is the output of the system. 



In general, if 
$$x(t) \in R ^{n}$$
$$u(t) \in R ^{m}$$
$$y(t) \in R^p$$
that means we get 

$$x'  - f(x, n)$$
$$y = \mathcal{L}(x, u)$$
which implies 
$$f: R^{n}\times R^{m} -> R^n$$
$\mathcal{L}: R^{n}\times R^{m} -> R^p$

#### Example 
$$x = \begin{bmatrix}x_{1} \\ x_{2} \end{bmatrix} \in R^2$$
where $u\in R$ and $y \in R$

We get, 
$$x' = \begin{bmatrix}x_{2} \\ -C\frac{x_{2}}{m} + \frac{u}{m} \end{bmatrix} $$
$$y = x_{1}$$

