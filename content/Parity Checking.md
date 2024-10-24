## Single Bit Parity 
Useful for detecting *single bit* errors. Add a bit at the end that ensures that the data has even parity.

*Even Parity* -> set parity bit so there's an even number of ones 
![[Pasted image 20241024133522.png]]

## Two-dimensional bit parity 
Detect and *correct* single bit errors. 
Here, we add a *parity bit* for each row and column which helps detecting two-bit errors and also *corrects* single bit errors without retransmission. 

![[Pasted image 20241024133653.png]]
![[Pasted image 20241024133708.png]]
![[Pasted image 20241024133717.png]]



This is still too limited as errors usually come in a burst. 

