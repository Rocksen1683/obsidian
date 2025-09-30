### [[Bayes Optimal Classifier]]

### Assumption on Data 
$$Pr_{y \sim Dy|X}[y = c | X] \approx Pr_{y \sim D|X}[y = c|X']$$ when $X$ and $X'$ are close. This means that when two distributions are close, they are probably similar and should be classified the same way.

### Algorithm

![[Pasted image 20250922130711.png]]


### Properties
- A *non-parametric* method 
- The hyperparameter $k$ is selected based on the dataset 

When $k$ is set too low it performs badly (purple line is bayes optimal classifier):
![[Pasted image 20250922132026.png]]

When $k$ is set too high, it also performs badly
![[Pasted image 20250922132051.png]]


### Time and Space Complexity 

**Train:** 0 time, $O(nd)$ space
the space is bad because you have to store the whole dataset 

**Test:** $O(ndk)$ time $\longrightarrow$ $O(nd)$ time and $O(nd)$ space 
the test inference time is slow as we have to go through the whole dataset so is not the best if you care about fast models 


[[k-Nearest Neighbour]] performs decently with [[MNIST]] with around 3% test error rate, which is really good for such a simple method. 


### Theorem 
Suppose
$$n \longrightarrow \infty, L_{1NN} \leq 2L_{Bayes}(1 - L_{Bayes})$$
where $L$ is the loss for a classification model.


