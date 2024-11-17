*Nonlocal Exceptions* are exceptions raised by a source execution at a failing execution and are only possible as every [[Coroutine]] has its own stack. 

You can raise [[Nonlocal Exceptions]] using `_Resume ... _At ...`

![[Pasted image 20241030163512.png]]

Non local delivery is initially *disabled* for coroutines but can be explicitly *enabled* using `_Enable`