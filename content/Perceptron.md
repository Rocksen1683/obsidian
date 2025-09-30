Perceptron is an algorithm for **online** [[Binary Classification]].

Implicitly, we assume that the data comes in the form such that we have a modified vector is the inner product of the feature vector $x_{i}$ and the weights vector $w$ and add some bias $b$ if necessary. We then take the `sign()` of the function and compare to the label. 

![[Pasted image 20250904140944.png]]

![[Pasted image 20250904152544.png]]

**Note:** `sign()` is the [[Signum Function]]

The goal is to come up with a separator (the sloped line in the graph) that splits the data into two halves. 

$$w = w + y_{I_{t}}x_{I_{t}} $$
is only updated in the case of a mistake when the value is less than the threshold $\delta$.

Anything above the line is categorized as $+1$ and below is $-1$. 

**Note:** Typically initialize $w = 0$, $b = 0$, and set $\delta = 0$
x
[[Perceptron Padding + Pre-Multiplication]]
[[Linear Seperability]]
[[Perceptron Error Bound]]

## Properties of Perceptron
### Uniqueness
- Perceptron only guarantees finding some solution (may be many) 
- Certainly not the “best” solution (draw picture)
- Support Vector Machines (SVMs) is better

### If data is not linearly seperable
- The algorithm will never halt, perceptron will cycle
- Not the best algo for non linearly separable data 

### Multiclass Classification
Instead of training one perceptron, we would train $k$ classifiers for different categories 
- Example one for dog vs not dog, one for cat vs not cat etc. 
- Output prediction is $arg$ $max_{i}<z_{i}, x>$ for the label point $x$

![[Pasted image 20250909140204.png]]
