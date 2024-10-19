### Example 1 
Say you have a pendulum with state 
$$x = \begin{bmatrix} \theta \\ \dot{\theta} \end{bmatrix} \in R^{2}$$
with *input*  $u = \tau \in R$ and output $y = \theta \in R$
After [[Linearization]], around $\bar{x} = \begin{bmatrix} 0\\ 0 \end{bmatrix} \in R^{2}$  and $\bar{u} = 0$

This gives us 
$$x = \begin{bmatrix} 0 & 1 \\ \frac{-g}{l}0 \end{bmatrix}x + \begin{bmatrix} 0 \\ 1 \end{bmatrix}u$$
$$y = \begin{bmatrix}1 & 0 \end{bmatrix}x$$

Now, computing the [[Transfer Function]], we get 
$$G(s) = \frac{\mathcal{L}(y(t))}{\mathcal{L}(u(t))} = \frac{Y(s)}{U(s)}$$
$$G(s) = (C(sI - A)^{-1}B + D)$$
$$= \begin{bmatrix} 1 & 0\end{bmatrix}(s\begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} - \begin{bmatrix} 0 & 1 \\ \frac{-g}{l} && 0 \end{bmatrix})^{-1}\begin{bmatrix} 0 \\ 1 \end{bmatrix} + 0$$
Now, we take the [[Inverse of a Matrix]]
which gives us 
$$= \begin{bmatrix} 1 & 0\end{bmatrix}(\frac{1}{s^{2} + \frac{g}{l}}\begin{bmatrix} s & 1 \\ \frac{g}{l} & s\end{bmatrix})\begin{bmatrix} 0 \\ 1 \end{bmatrix} + 0$$

$$= (\frac{1}{s^{2} + \frac{g}{l}})\begin{bmatrix} s & 1\end{bmatrix}\begin{bmatrix} 0 \\ 1 \end{bmatrix}$$
This gives us 
$$G(s) = \frac{1}{s^{2} + \frac{g}{l}}$$
The reason that calculating the *transfer function* makes it easier to get output from input 

$$y(t) = \mathcal{L}^{-1}(G(s)\mathcal{L}(u(t)))$$
$$ y(t) = \mathcal{L}^{-1}(\frac{1}{s^{2} + \frac{g}{l}}(\frac{1}{s}))$$
This is a [[Real Rational TF]] :) 

In our transfer function $G(s)$, we have 
$b_{0} = 1$  and $b_{i} = 0$ (numerator)
$a_{0} = \frac{g}{l}$ and $a_{1}= 0$ and $a_{i} = 0, i > 3$  (denominator)
So this T.F is both *proper* and *strictly proper*

Now, calculating the [[Poles and Zeros]], we get:

Zeros: No zeros 
Poles: $j\sqrt{\frac{g}{l}}, - j\sqrt{\frac{g}{l}}$


### Example 2 
Say we have a [[Graphs]], with some *nodes* and *edges*. Say we have a node $TS$ with 5 edges (1-5) and another node $EM$ with 3 edges (6, 7, and 8).

We are trying to move the whole $TS$ to $EM$

$$ u = \begin{bmatrix} u_{TS} \\ u_{EM}\end{bmatrix}$$
$$\dot{x_{TS}} = u_{TS}$$
$$\dot{x}_{EM} = u_{EM}$$
$$\dot{x}_{i} = x_{TS} - x_{i}, i \in \{1...5\}$$
$$\dot{x}_{j} = x_{EM} - x_{J}, J \in \{6...8\}$$

$$\dot{x} = \begin{bmatrix} \dot{x_{TS} }\\ \dot{x}_{EM} \\ x_{1} \\\ x_{2} \\ ... \\ x_{8} \end{bmatrix} = -Lx + \begin{bmatrix}1 & 0 \\ 0 & 1 \\ 0 \end{bmatrix}u$$
 where $L$ is the [[Laplacian Matrix]] of a graph 
### Example 3 
Let us consider an example with a *queue*, 
]where $\dot{q}$ is the length of the queue and $u$ is the arrival rate and $s$ is the service rate (a constant).
$$\dot{q} = u - s$$
$$x = q$$
$$\dot{x} = u - s$$
which gives our $f(x, u)$
Now when we see the equilibrium point
$$f(\bar{x}, u) = 0$$
this gives us 
$$\bar{u} - s = 0 \implies \bar{u} = s$$
and some $\bar{x} = 0$
Now [[Linearization]] this, we get 
$$f(x, u) = u - s$$
which means 
$$\delta\dot{x} = \delta u$$
After dropping deltas, we get 
$$\dot{x} = u$$
We want to measure the output $y = x$

The transfer function $G(s)$ will be:
$$G(s) = (C(sI - A)^{-1}B + D)$$
$$= 1(s - 0)^{-1}1 + 0 $$
$$ = \frac{1}{s}$$
$$Y(s) = 1U(s)$$
$$y(t) = \int_{u}^{t}u(\tau)d\tau$$
$$q(t) = y(t) = \int_{0^t}u(\tau)d\tau$$
$$ = \int_{0}^{t} (u(\tau) - s(\tau))d\tau$$
