Assuming that in a *feedback loop system* with transfer function $F(s)$ such that 
$$F(s) = \frac{G(s)}{1 + G(s)}$$
We know that based on [[Stability of Interconnected Systems]], that $G(s)$ being stable does not imply that $F(s)$ is stable (and vice-versa). 

To help make it easier to check whether $F(s)$ is stable, we can design an algorithm to check whether the *roots* of a polynomial are in the left half of the complex plane ($C^{-}$) without actually computing them. 

## [[Routh Array]]
## [[Hurwitz Polynomial]]


Now, the [[Routh-Hurwitz Criterion]] for stability says, that all of the terms in the *first column* of the [[Routh Array]] must have the same sign and that the polynomial is a [[Hurwitz Polynomial]]. 


## Examples
Examine stability of the given equations using [[Routh-Hurwitz Criterion]]:

$$ s^{3}+ 6s^{2}+ 11s + 6 =0$$
We can say that the above polynomial is a[[Hurwitz Polynomial]] :) 

![[Pasted image 20241202131912.png]]

We can verify that this polynomial is stable :) 