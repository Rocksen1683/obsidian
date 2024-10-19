Making *non-linear* systems into a *linear* approximation to help solve a particular control system. 

Linearizing $\dot{x}  = f(x, u)$ and $y=h(x, u)$
1. Select an [[Equilibrium Point]] $(x^{-}, u^{-}) \in R^{n} \times R^{m}$ such that $y^{-} = h(x^{-}, u^{-}). f(x^{-}, u^{-}) = 0$
2. Compute [[Jacobians]] of $f, h$ to get $A, B, C, D$
3. Linearization: $\dot{\partial x} = A\partial + B \partial u, \partial y= C \partial x + D\partial u$
