Initialize $w_o$
For $t = 1, 2, ...$
- Choose direction $d_{t}$
- Step size $\eta_{t}$

$$w_{t} = w_{t-1} - \eta_{t} d_t$$

### How to pick eta
A common way to set $\eta_t$ would be the following
- **Constant** 
- **Decaying**
- **Adaptive**

### How to pick Direction
For example, for Gradient Descent, we pick the *direction* as the *gradient of the loss function*.

For [[Stochastic Gradient Descent]]: pick set $B \subseteq [n]$ randomly

For Newtons Method, 
![[Pasted image 20250929180208.png]]

