![[Pasted image 20241202153922.png]]
The goal of designing a controller $C(S)$ would be to design it in such a way such that the closed-loop system 
$$F(s) = \frac{Y(s)}{R(s)} = \frac{L(s)}{(1 + L(s))} = \frac{C(s)G(s)}{1 + C(s)G(s)}$$
would satisfy desired specifications.

To do so, we can break the design process into the following steps:
1. Turn specifications from the *time domain* to the *frequency domain*
2. Design the [[Transfer Function]] $C(s)$ so that $L(s) = C(s)G(s)$ has the desired frequency domain behaviour

![[Pasted image 20241202154612.png]]
## Control Specifications 
### Stability 
For stability, we would want [[Magnitude and Phase Gain]] $k_{m}> 0$ and $\delta_{m}> 0$

### Robust Stability
We would want high $k_m$ and high $\delta_m$ and would like to maximize
