Given a set $(x_{1}, y_{1})$ where
- $x_i$: is a feature vector $\implies x_{i}\in R^{d}$
- $y_{i}$: is a label $\implies y_{i}\in \{ -1, +1 \}$

The goal is to "learn" a function $h$ that maps $x_i$ to $y_{i}$. This means that $h(x) = y$

## Examples

![[Pasted image 20250904133912.png]]

![[Pasted image 20250904133932.png]]

### Statistical Learning
The goal would be to come up with a probability distribution $P$ such that we would. be able to learn $h$. Learning $h$ means that $R^{d}\longrightarrow \{-1, +1\}$ such that the $Pr_{(x,y) \~ P} [h(x) = y]$  is large.

$P$ can be any probability distribution, for example *bayes classifier*.
### Online Learning
![[Pasted image 20250904135554.png]]


