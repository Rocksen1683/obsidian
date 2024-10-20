A system 
$$\dot{x} = Ax + Bu$$
$$y = Cx + Du$$

is:
1. ***stable***: if for every initial condition $x(t_{0})= x_{0} \in R^{n}$, the $x(t) = e^{A(t-t_{0})}x_0$ (unique solution from [[Linear System Theory]]) is *uniformly bounded*
2. ***asymptotically stable***: if in addition to stable, for every initial condition $x(t_{0}) = x_{0}$, $x(t) \longrightarrow 0$ as $t \longrightarrow \infty$
3. ***unstable***: if it's not stable 
## [[BIBO Stability]]
### Asymptotic Stability Theorem
> The system is asymptotically stable $\iff$ All eigenvalues of $A$ have a negative real part

> Asymptotic Stability $\implies$ [[BIBO Stability]]

