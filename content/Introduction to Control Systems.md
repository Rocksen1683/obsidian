To come up with a control system, you need to:
1. Study the system (inputs/outputs, actuators/sensors)
2. Define control specifications (Meet target requirements)
3. Obtain a model of the system (using first principles, data)
4. Simplify the model ([[Linearization]])
5. Design the controller
6. Simulate the controlled system using the model (helps us verify that our system works as intended)

### Example 
Assuming we have a car system with a with a speed of $\frac{dp}{dt} = p'(t)$ and acceleration $\frac{d^{2}p}{dt^{2}}= p''(t)$
We end up with a relation 
$$mp''(t) + C(p'(t)) = f(t)$$
where $f(t)$ is the force in the forward direction and $C(p'(t))$ is the drag resistance and $m$ is the inertia. 


### [[State Space Form]]

For the above example, we can have the following representations of state 
$$x(t) = \begin{bmatrix} p(t)  \\ p'(t) \\ p''(t) \end{bmatrix}$$
### [[Equilibrium Point]]

In the case that you need to calculate the final value of some output signal, use [[Final Value Theorem]].

Also refer [[One-sided Laplace Table]] and [[Laplace Properties]] which will help solve problems :) 