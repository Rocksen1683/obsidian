So far, we've been looking at datasets that are [[Linear Seperability]] or have some sort of *linear* relationship. However, in general, this is not the case for most datasets and we would have more complex relationships. 

Let us consider that
- $x_{i}$ is the $i^{th}$ *coordinate*
- $x^{i}$ is the $i^{th}$ *datapoint*

Consider a dataset where we have all +1 points in a circle and all -1 points outside the circle. This dataset is not [[Linear Seperability]] but we can still draw a decision boundary that looks like 
$$x_{1}^{2}+ x_{2}^{2} \leq R$$
Now, consider a feature map
$$\phi(x): R^{2}\longrightarrow R^{3}$$
where 
$$\phi(x) = [x_{1}, x_{2}, x_{1}x_{2}]$$

### [[Feature Map]]

The standard SVM form is 
![[Pasted image 20250930150816.png]]

But replacing $x$ with a [[Feature Map]] $\phi(x)$, we get

![[Pasted image 20250930150749.png]]

Now computing the dot product will look like 
$$\phi(x) = [\vec{xx^{T}}, \sqrt2 x, 1]$$
$$<\phi(x), \phi(x')> = <\vec{xx^{T}}, \vec{x'x'^{T}}> + <\sqrt2 x,\sqrt2 x'> + <1, 1> $$
$$<\phi(x), \phi(x')> = 1 + 2<x, x'> + <x, x'>^{2}$$
$$<\phi(x), \phi(x')> = (<x, x'> + 1)^{2}$$


Now we define a *kernel function* as 
$$k(x, x') = (<x, x'> + 1)^{2}$$
which would do the quadratic [[Feature Map]] computation in $O(d)$ time instead of $O(d^{2})$

### Formal Definition of Kernel 
A *kernel* function is one that 
$$k: R^{d}\times R^{d} \longrightarrow R $$
if there exists a [[Feature Map]] $\phi: R^{d} \longrightarrow R^{m}$  ($m > d$) such that 
$$k(x, x') = <\phi(x), \phi(x')>$$

The [[Feature Map]] $\phi(x)$ may be expensive or impossible to compute but the [[Kernels]] $k$ *may be tractable*

### [[Polynomial Kernel]]

### [[Gaussian Kernel]]

### What makes a valid kernel?
If we can construct a corresponding feature map $\phi$

![[Pasted image 20250930152545.png]]

### [[Using Kernels in SVM]]