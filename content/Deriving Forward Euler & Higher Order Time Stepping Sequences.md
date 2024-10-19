## Deriving F.E
### Approach 1: Approximate the derivative using a finite difference 

**ODE Form:**
$$y'(t) = f(t,y(t))$$
Finite difference approximation of $y'$ gives: 
$$y'(t_{n}) \approx \frac{y_{n+1}- y_{n}}{t_{n+1}-t_{n}}$$
So 
$$y'(t_{n}) \approx \frac{y_{n+1} - y_{n}}{n}= f(t_{n}, y)$$
Rearrange to get the *Forward Euler*: 
$$y_{n+1} = y_{n}+hf(t_{n}, y_{n})$$
where $h = t_{n+1}- t_n$

### Approach 2: Truncate a Taylor Series by dropping higher order terms
Standard Taylor Series is: 
$$f(x) = f(a) + f'(a)(x-a) + \frac{f''(a)}{2!}(x-a)^{2}+\frac{f'''(a)}{3!}(x-a)^3$$
We want to approximate $y(t_{n+1})$ based on $t_n$ so: 
$$y(t_{n+1)}= y(t_{n)}+ y'(t_n)(t_{n+1}-t_n) + \frac{y''(t_{n})}{2!}(t_{n+1}-t_{n})^{2}+\frac{y'''(t_{n})}{3!}(t_{n+1}-t_{n})^3$$
We have replaced $f \rightarrow a, a \rightarrow t_{n,}x \rightarrow t_{n+1}$ or
$$y(t_{n+1)}= y(t_{n)}+ y'(t_n)h + \frac{y''(t_{n})}{2!}(h)^{2}+\frac{y'''(t_{n})}{3!}(h)^3$$
As $h = t_{n+1}- t_{n}$ .
Assume that terms of $h^2$ and higher will be smaller as $h \rightarrow 0$, so we drop them and replace $y'$ with an evaluation of $f$ (slope) to give the *Forward Euler*:
$$y(t_{n+1}) \approx y_{n+1} = y_{n}+ hf(t_{n}, y_{n})$$

## Error of Forward Euler
![[Pasted image 20240131132700.png]]
#### Understanding forward Euler error
*Forward Euler* makes a linear approximation at each step, incurring a "local" error. 

Smaller step size $h \rightarrow$ more frequent slope estimates $\rightarrow$ less error

### Local Truncation Error

*Forward Euler* is 
$$y_{n+1} = y_{n}+hf(t_{n}, y_{n})$$
Taylor series was: 
$$y(t_{n+1)}= y(t_{n)}+ y'(t_n)h + \frac{y''(t_{n})}{2!}(h)^{2}+\frac{y'''(t_{n})}{3!}(h)^{3} + ...$$
The error for *one step* is the difference between these, assuming exact data at time $t_n$. That is, 
$$y_{n}= y(t_n)$$
In that case, the F.E's expression becomes 
$$y_{n+1}= y(t_{n}) + hf(t_{n}, y(t_{n}))$$
we know that
$$= y(t_{n}) + hy'(t_{n})$$
The difference is 
$$y_{n+1} - y(t_{n+1}) = \frac{-h^{2}}{2}y''(t_{n}) + O(h^{3})$$
**NOTE:** Big $O$ , in this course is different in this course. In general we, take $n \rightarrow \infty$ **BUT**  in this course, we take $n \rightarrow 0$ as we are measuring error. 

So, this
$$y_{n+1} - y(t_{n+1}) = \frac{-h^{2}}{2}y''(t_{n}) + O(h^{3})$$
evaluates to 
$$O(h^2)$$
This is the *Local Truncation Error* or **LTE**. 
As $h$ decreases, the error (for one step) decreases *quadratically*. 

## Trapezoidal Method 
### Derivation
Taylor Series is 
$$y(t_{n+1)}= y(t_{n)}+ y'(t_n)h + \frac{y''(t_{n})}{2!}(h)^{2}+O(h^2)$$
Approximate $y''(t)$ as 
$$\frac{y'(t_{n+1})-y'(t_{n})}{h}+ O(h)$$
and plug in: 
$$y(t_{n+1)}= y(t_{n)}+ y'(t_n)h + \frac{h^2}{2!}\frac{y'(t_{n+1})-y'(t_{n})}{h}+ O(h)+O(h^2)$$
Simplify: 
$$y(t_{n+1})= y(t_{n)}+ y'(t_n)h + \frac{h^2}{2!}\frac{y'(t_{n+1})-y'(t_{n})}{h}+ O(h)+O(h^2)$$

This suggests the *trapezoidal scheme:*
$$y_{n+1} = y_{n} + \frac{h}{2}[f(t_{n}, y_{n}) + f(t_{n+1}, y_{n+1})]$$
