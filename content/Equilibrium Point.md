$(x^{-}, u^{-}) \in R^{n} \times R^{m}$ is an equilibrium point if 
$$
f(x^{-}, u^{-}) = 0
$$

This means that 
$$x' - f(x^{-}, u^{-}) = 0$$
$$x(t) = x^{-}$$
$$u(t) = u^{-}, t\in [t_{0}, t_{1}]$$
This means that $x(t) = x^{-}$ is a solution 

$$x' = f(x, u)$$
$$x(t_{0}) = x^{-} + \delta x^{-}$$
$$u(t) = u^{-} + \delta u(t)$$
### Example 
$$\frac{dx}{dt} = z$$
$$\frac{dz}{dt} = -z - \sin x$$
where $x, z$ are the [[State Space Form]] of a system. 

The ***equilibrium points*** would be the points when 
$$\frac{dx}{dt} = 0 \implies z = 0$$
$$\frac{dz}{dt} = 0 \implies -z - \sin x = 0$$
$$\implies -\sin x = 0$$
$$\implies x = \pm n \pi$$
where $n = 0, 1, 2, 3, ...$
Therefore, the [[Equilibrium Point]] are:
$$x^{*} = \pm n\pi; n = 0, 1, 2,...$$
$$z^{*} = 0$$

