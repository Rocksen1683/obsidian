We are not sure if the [[Perceptron]] algorithm even converges. So it will only converge for [[Linear Seperability]] datasets with the following error bound. 

Suppose there exists some weith vector and vias $z = (w, b)$ such that $Az \geq s\vec{1}$ (*linearly seperable*). Then the [[Perceptron]] algorithm will correctly classify the entire dataset after at most
$$\frac{R^{2}||z||^{2}_{2}}{s^{2}}$$

where 
- $R = max(||a_{i}||_{2})$
- and $||x||_{2}$ is the [[Euclidean Norm]]

There might be many valid $z, s$ that would separate the dataset which means that this algorithm provides non-unique solutions. 

The solution that will provide the least number of mistakes would be the one that minimizes 
$$\frac{||z||^{2}_{2}}{s^{2}}$$
and thus the number of mistakes.

![[Pasted image 20250909133809.png]]

***Margin*** is defined as $\gamma ^ {2}$
- Larger margin $\implies$ easier to classify as fewer errors due to large margin
- Smaller margin $\implies$ harder to classify as larger errors

