## Cubic splines *via* Hermite Interpolation 
**Strategy:** Use Hermite interpolation as a stepping-stone to build a cubic spline!

![[Pasted image 20240122130727.png]]
![[Pasted image 20240122130854.png]]

Start from Hermite closed form in $i^{th}$ interval
$$S_i'(x)= a_{i}+ b_i(x-x_{i)}+ c_i(x-x_i)^2+d_i(x-x_i)^3$$
It's 2nd derivative is: 
$$S_i''(x)= 2c_{i}+ 6d_{i}(x-x_{i)}= 2(\frac{
3y_{i}- 2s_{i}-s_{i+1}}{\Delta x_{i}}) + (\frac{s_{i}+s_{i+1}- 2y_{i}'}{\Delta x_{i}^2})(x - x_{i})$$
Let $s_{i}$'s be unknowns. To face matching 2nds derivates at the knot/node between intervals $i$ and $i+1$ , set ... 
$$S_{i}''(x_{i+1}) = S_{i+1}''(x_{i+1})$$
for $i = 1$ to $n-2$
$$S_i''(x_{i+1})= 2(\frac{
3y_{i}- 2s_{i}-s_{i+1}}{\Delta x_{i}}) + (\frac{s_{i}+s_{i+1}- 2y_{i}'}{\Delta x_{i+1}^2
})(x - x_{i})$$
Estimate this to get conditions on the slopes $s_i$ at each knot. 
We find 
$$\left(\frac{2s_{i}+4s_{i+1} - 6y_{i}'}{\Delta x_{i}}\right)=\left(\frac{6y_{i+1}' - 4s_{i+1}-2s_{i+2}}{\Delta x_{i+1}}\right) $$
Cross-multiply and take $s_i$ to the *LHS* 
$$\Delta x_{i+1}s_{i}+ 2(\Delta x_{i}+ \Delta x_{i+1})s_{i+1} + \Delta x_{i}s_{i+2}$$
Reindex $i \rightarrow i+1$ so we have one equation per inner know $i$. 
for $i=2$ to $n-1$: 
$$\Delta x_{i+1}s_{i-1}+ 2(\Delta x_{i-1}+ \Delta x_{i})s_{i} + \Delta x_{i-1}s_{i+1} = 3(\Delta x_{i}y_{i-1}+ \Delta x_{i-1}y_{i}')$$
Now, we just need *boundary conditions* :) 

## Boundary conditions for Efficient Cubic Splines 
We need conditions (equations)  for $i= 1$ and $i = m$ to complement the $n-2$ interior equations. 
Since we have $n$ unknowns (the $s_i$'s), we can have the following methods 
1. [[Clamped Boundary Conditions (given slope)]]
2. [[Natural/Free Boundary Conditions]]
## Efficient Cubic Splines - Matrix Form 
![[Pasted image 20240122135452.png]]

#### Example Problem 1 

![[Pasted image 20240122135546.png]]

First, we have to compute the $\Delta x_i$'s and $y_i'$ for $i=1$ to $3$. 
$$\Delta x_{1} = 2 - 0 = 2 $$
$$\Delta x_{2} = 3 - 2 = 1 $$
$$\Delta x_{3} = 4 - 3 = 1 $$
$$y_{1}' = \frac{1-1}{2}= 0$$
$$y_{2}' = \frac{3-1}{1}= 2$$
$$y_{3}' = \frac{-1-3}{1}= -4$$
Now, we find the equations/rows: 
for $i = 1$ to $4$ (one per node)
$i = 1: s_{1}= 1$ so $T_{i} = \begin{bmatrix}1 & 0 & 0 & 0 \end{bmatrix}$ and $r_{1}= 1$
$i = 2$:
$$$$$$\Delta x_{2}s_{1}+ 2(\Delta x_{2}+ \Delta x_{1})s_{2} + \Delta x_{1}s_{3
} = 3(\Delta x_{2}y_{1}'+ \Delta x_{1}y_{2}')$$


plugging in the values gives us: 

$$T_{2} = \begin{bmatrix}1 & 6 & 2 & 0 \end{bmatrix}$$

Solving the same eqns for $i=3$ and $i = 4$, we get $T_{3}$ and $T_4$. The final matrix would be: 
$$T = \begin{bmatrix}1 & 0 & 0 & 0 \\
1 & 6 & 2 & 0\\
0 & 1 & 4 & 1\\
0 & 0 & 0 & 1 \\
 \end{bmatrix}, r = \begin{bmatrix}1 \\ 12 \\ -6 \\ -1 \end{bmatrix}$$

### Matrix Size and Structure

![[Pasted image 20240122141028.png]]
![[Pasted image 20240122141044.png]]
![[Pasted image 20240122141059.png]]

#### Example Problem 2 
![[Pasted image 20240122141251.png]]
Here, we only need to check the interpolating and derivative conditions.  Since no boundary conditions are given. 
**How to solve:**
- 