A bayes classifier is a goal for classification and is used as a benchmark for classification machine learning problems. 

The goal in classification is to solve 
$$min_{f}Pr_{x, y \sim D}[f(x) \neq y]$$

where 
- $x \in X$ is the data domain 
- $y \in Y$ is the label space, eg: $\{0, 1\}$
- $(x, y) \sim D$ is the unknown distribution 
Due to $D$ being unknown, we try to optimize the loss on the training set as a proxy for optimizing wrt to $D$

We can decompose $D$ in the following way:
- $D_{x}$: is the *margin* over data domain
- $D_{y | X=x}$ : is the *conditional distribution* when conditioning on receiving a particular domain element 

![[Pasted image 20250916132646.png]]

![[Pasted image 20250922125715.png]]

