All pages have an additional bit called the *use bit*. The algorithm works like this:
- when a page is loaded into a frame, the *use bit* is set to $1$
- during replacement, we check all of the *use bits*
	- if $1$, we set it to 0 
	- if $0$, we replace 
	- if all are $1$, we set everything to $0$ and take first one

### Example 
![[Pasted image 20240311011314.png]]
![[Pasted image 20240311013914.png]]
