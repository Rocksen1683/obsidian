Given a recurrence relation of the form 
$$T(n) = a T\left(\frac{n}{b}\right)+ \Theta(n^{y})$$
where $a \geq 1, b > 1$, we can say the following if we denote $x = \log_{b}^{a}$
- $T(n) \in \Theta(n^{x})$ if $x > y$
- $T(n) \in \Theta(n^{y}\log n)$ if $x = y$
- $T(n) \in \Theta(n^y)$ if $y > x$
