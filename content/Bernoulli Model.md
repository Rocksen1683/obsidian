$$Pr[Y= 1|X, w] = P(X, w) \in [0, 1]$$
$$Pr[Y=0|X, w] = 1 - P(X, w)$$
where $0$ and $1$ are the *labels* of classification. 

Take $1$:
$$P(X, w) = <x, w>$$
this means that if the dot product is *large* and is on one side of the hyperplane, we have a positive score and if it is *small* and is on the other side of the plane, we have a negative score. 

This captures the *confidence* but not in probability terms. 

Instead, we take the [[Logic Transform]] and get 
$$log\left( \frac{P(X,w)}{1 - P(X, w)} \right) = <X, w>$$
Taking exponent on both sides:

$$\frac{P(X, w)}{ 1- P(X, w)} = exp(<X, w>)$$
This is called the *odds ratio* of the probability that a point is labelled $1$ (which is $P(X, w)$) by the probability that a point is labelled $0$ (which is $1- P(X, w)$). 

Solving this equation, we get 
$$P(X, w) = \frac{exp(<X, w>)}{1 + exp(<X, w>)}$$
Multipling the top and bottom by $\frac{1}{exp(<X, w>)}$, we get 
$$P(X, w) = \frac{exp(<X, w>)}{1 + exp(<X, w>)} = \frac{1}{1 + exp(-<X, w>)}$$
which is called the [[Sigmoid]] function. 

So, we can say that the 
$$P(X, w) = sigmoid(<X, w>)$$
