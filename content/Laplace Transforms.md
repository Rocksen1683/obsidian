
[[One-sided Laplace Table]]
### Example for why we care about Laplace 
Use the Laplace Transform to solve the IVP 
$$y' = \sin(t), y(0) = 0$$
$$\mathcal{L}\{y'\} = \mathcal{L}\{\sin t\}$$
$$s Y(s) - Y(0) = \frac{1}{s^{2}+ 1}$$
$$\implies Y(s) = \frac{1}{s(s^{2}+ 1)} = {\frac{1}{s(s^{2}+1)}}$$
$$ = \frac{1}{s}- \frac{s}{s^{2}+1}$$
$$Y(t) = \mathcal{L}^{-1}\{\frac{1}{s}- \frac{s}{s^{2}+1}\} = \mathcal{L}\{\frac{1}{s}\}- \mathcal{L}\{\frac{s}{s^{2}+1}\}$$

### Example 2 
Use the Laplace table to compute 
$$\mathcal{L}^{-1}\{\frac{1}{s-3}+ \frac{s}{s^{2}-4}\}$$
**Solution:**
$$\mathcal{L}^{-1}\{\frac{1}{s-3}\} + \mathcal{L}^{-1}\{ \frac{s}{s^{2}-4} \}$$
$$= \mathcal{L}^{-1}\{\frac{1}{s-3} | _{s-3}\} + \cosh(2t)$$
$$ = e^{3t}.1 + \cosh(2t)$$

### Example 3 
Use the Laplace table to compute 
$$\mathcal{L}\{e^{2}t - \sin(4t) + 6t^{3}\}$$
**Solution:**
$$e^{2}\mathcal{L}\{t\} - \mathcal{L}\{\sin 4t\} + 6\mathcal{L}\{t^3\}  $$
$$= \frac{e^{2}}{s^{2}}- \frac{4}{s^{2}+16}+6\frac{3!}{s^{4}}$$
