The following performance metrics quantitatively describe the behaviour of a system based on it's output response, $y(t)$ to a unit step input signal. 

These metrics are:
![[Pasted image 20241020171552.png]]
### Steady State Gain
The steady state value of $y(t)$, which will be:

$$C_{ss} = \lim_{t \longrightarrow \infty} y(t)$$
### Rise Time 
$T_{r}$ is defined as 
$$T_{r} = t_{1} - t_{2}$$ where $t_{1}, t_{2}$ are the *smallest times* such that the output is $10\%$ and $90\%$ of the *steady state*. 

### Peak Time 
$T_{p}$ is defined as the time instant at which the peak $C_{max}$ is achieved 

### Overshoot Percentage
$OS\%$ is defined as 
$$OS \% = \frac{|C_{max}| - C_{ss}}{ C_{ss}}(100)$$
### Settling time 
$T_{s}^{\epsilon \%}$ is the smallest $T$ such that 
$$\forall t \geq T, \frac{|C_{ss} - y(t)|}{|C_{ss}|} \leq \epsilon$$

## [[Approximate Expressions of Performance Metrics]]