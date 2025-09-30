## Problem
$$min_{w,b} \frac{1}{2} ||w||^{2}_{2}, s.t: y_{i}(<w,x_{i}> + b) \geq 1$$
Instead of keeping $||w||_{w}$ fixed and maximizing $\gamma$, we should do the opposite.

Let $\widehat{y_{i}} = <w, x_{i}> + b$, where the *sign* of $\widehat{y_i}$ gives the *prediction*
$$min_{w,b} \frac{1}{2} ||w||^{2}_{2}, s.t: y_{i}\widehat{y_{i}} \geq 1$$

When we *compare* with the writing of [[Perceptron]] 's objective which is 
$$min_{w,b} 0, s.t: y_{i}\widehat{y_{i}} \geq 1$$

We end up with $0$ 
With this, we can say that the [[Hard-Margin SVM]] is the [[Regularization]] of [[Perceptron]]'s objective. 

## Dual Formulation Derivation
We know that the *primal-formulation* of SVM is the following
$$min_{w,b} \frac{1}{2} ||w||^{2}_{2}, s.t: y_{i}(<w,x_{i}> + b) \geq 1$$

We observed that it is a *[[Constrained Optimization Problem]]* and can be converted to an [[Unconstrained Optimization Problem]] by using a [[Lagrange Multiplier]]

This ends up as 
$$min_{w, b} \; max_{\alpha \in R^{n}, \alpha\geq 0} \; \frac{1}{2} ||w||^{2}_{2} - \sum\limits_{i=1}^{n} \alpha_{i}(y_{i}(<w, x_{i}> + b) - 1)$$
Now due to [[Strong Duality]], we can swap the *max* and *min* to get 
$$max_{\alpha \in R^{n}, \alpha\geq 0} \; min_{w, b} \; \frac{1}{2} ||w||^{2}_{2}- \sum\limits_{i=1}^{n} \alpha_{i}(y_{i}(<w, x_{i}> + b) - 1)$$
Fix some $\alpha$ for now and solve the inner minimization by setting the *gradient* to $0$. 

$$\frac{\partial}{\partial b} = - \sum\limits_{i} \alpha_{i}\gamma_{i} = 0$$
$$\frac{\partial}{\partial w} = w- \sum\limits_{i} \alpha_{i}y_{i}x_{i} = 0$$

with this, we can say that 
$$ \sum\limits_{i} \alpha_{i}\gamma_{i} = 0$$
and
$$ w = \sum\limits_{i} \alpha_{i}y_{i}x_{i}$$
Substituting this in the above equation, we get 
![[Pasted image 20250923141208.png]]

$$min_{\alpha \in R^{n}, \alpha\geq 0} \; \frac{1}{2} ||\sum\limits_{i} \alpha_{i}y_{i}x_{i}||^{2}_{2}- \sum\limits_{i=1}^{n} \alpha_{i}(y_{i}(<w, x_{i}> + b) - 1)$$

The *min* shows up as we negate the whole equation. 

## Interpreting Hard SVM Solution
![[Pasted image 20250923142305.png]]\
