Assuming that in a *feedback loop system* with transfer function $F(s)$ such that 
$$F(s) = \frac{G(s)}{1 + G(s)}$$
We know that based on [[Stability of Interconnected Systems]], that $G(s)$ being stable does not imply that $F(s)$ is stable (and vice-versa). 

To help make it easier to check whether $F(s)$ is stable, we can design an algorithm to check whether the *roots* of a polynomial are in the left half of the complex plane ($C^{-}$) without actually computing them. 

