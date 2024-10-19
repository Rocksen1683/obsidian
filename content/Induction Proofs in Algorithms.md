## Example 
Prove: 
$$T(n) \leq T(\frac{n}{5})+ T\left(\frac{7n}{10}+ 6\right) + O(n) : n > 120$$

**Solution:**
We show that $T(n) \leq cn$ for a large enough $c$ and  all $n > 0$:
We know that if $c$ is large enough, then $T(n) \leq cn$ for all $n < 120$.

Chose a constant $a$ to write $O(n)$ as $an$. 
Assume the statement $T(m) \leq cm$ for all values $0 < m < n$ . We have: 
$$T(n) \leq c\left(\frac{n}{5}\right)+ c\left(\frac{7n}{10}+6\right)+ an \leq \frac{cn}{5}+ \frac{7cn}{10}+6c + an$$
$$= \frac{9cn}{10}+ 6c + an = cn + \left(\frac{-cn}{10}+6c + an\right)$$
We need a condition such that:
$$ \left(\frac{-cn}{10}+6c + an\right) \leq 0$$
which would imply that it would be smaller than $cn$ too. 
Solving the above inequality, we get: 
$$c\left(6 - \frac{n}{10}\right)+ an \leq 0 \iff c\left(6 - \frac{n}{10}\right) \leq -an$$
$$c\left(\frac{n}{10} - 6\right) \geq an \iff c \geq 10a\left(\frac{n}{n-60}\right)$$
Now if $n > 120$ then we have 
$$\frac{n}{n-60} \leq 2$$
and we can choose 
$$c \geq 20a \geq 10a\left(\frac{n}{n-60}\right)$$

**Intuition for choosing 120:** There are only a finite number of values from 1 to 120. Good thing to do is to take a value and double it to make sure $c$ is large enough. 

