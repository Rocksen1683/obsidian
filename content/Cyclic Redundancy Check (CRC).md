A more powerful approach to [[Link Layer Error Detection]]. Involves the computation of the following 
- $D$: *data bits* 
- $G$: *bit pattern* (generator) of $r+1$ bits 

![[Pasted image 20241024133942.png]]

We would want to use the following formula for bit pattern: 
$$G = <D, 2^{r}> \oplus R$$
where $\oplus$ is $XOR$ and $<D, 2^{r}>$ is left shifting by $r$

The *sender* computes $r$ CRC bits, $R$, such that $<D, R>$ is exactly divisible by $G$ (mod $2$)

The *receiver* knows $G$ and divides $<D, R>$ by $G$. In the case of a *non-zero remainder*, we know that an error is detected 


With this, we can detect all burst errors in less than $r+1$ bits and this method is widely used in things like Ethernet and WiFi.

## Example 
![[Pasted image 20241024134610.png]]
