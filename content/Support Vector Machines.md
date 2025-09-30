## Setting
Given $(x_{i}, y_{i})$ pairs where $x_{i} \in R^{d}$ and $y_{i}\in \{ -1, +1\}$
We assume that the dataset is [[Linear Seperability]]

Thinking about the data we had in [[Perceptron]], the solution we get is a separator between  different classifications. Our goal here is to find the *best classifier* which is what [[Support Vector Machines]] aim to do. 

## Margins
Suppose we have a perceptron solution $w', b'$ where $w$ is the *weight* and $b$ is the *bias*. We know that the perceptron solution is *non-unique* and we can have infinite number of solutions. 

### Claim
Let us assume that $||w'||_{2} = 1$, then the distance from point $i$ to the hyperplane is 
$$\gamma_{i} = y_{i}(<w', x_{i}> + b')$$
This quantity $\gamma_{i}$ can be computed for any points ($x_{i}, y_{i})$ and represents the distance between that point to the *classification line*. 

The *margin* of a dataset is the $\gamma$ such that 
$$\gamma = min_{i}\gamma_{i}$$
The [[Perceptron]] problem aims to find any $w', b'$ such that $min_{i}\gamma_{i} \geq 0$ 

However with [[Support Vector Machines]], we aim to *maximize* the margin which corresponds to the line of classification that is the most in the middle between the two classifications. 
## SVM Goal 

The goal would be to *maximize* the *minimum* of $\gamma_{i}$ and we know that the min of gamma is the margin, so our goal is simply to *maximize the margin*. 

Having to satisfy the conditions of [[Perceptron]],  we can formalize our goal as 
$$argmax_{w', b'} (\gamma)$$
such that
$$y_{i} (<w', x_{i}>) + b) \geq \gamma$$
where 
$$\gamma = min_{i}\gamma_{i}$$
### Deriving Problem
![[Pasted image 20250923132856.png]]

The $\frac{1}{2}$ is mainly to account for *gradient*.

The last step is due to turning the problem from a [[Concave Problem]] to a [[Convex Problem]]
. We are also adding a *squared* of the norm as it does not change anything with respect to the *min* but will make it easier for the *optimization problem*. It also makes it [[Strongly Convex]] which also makes it easier. 

We also remove the $\gamma$ because it's not as important in terms of the optimization and won't affect anything. 
## [[Hard-Margin SVM]]

## [[Soft-Margin SVM]]