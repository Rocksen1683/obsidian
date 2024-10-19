Select test cases while being *modification-aware*

 [[Regression Testing]] uses this. 

*Modification-Revealing Test* : A test that produces a different output with $P'$ and actually reveals the modification. This means that it needs to execute some code modified from $P$ and $P'$

*Inclusiveness:*  If $T$ contains $n$ modification-revealing tests and $S$ contains $m$, then *inclusiveness* of $S$ is $m/n$

*Precision:* If $T$ contains $n$ non-modification-revealing tests and $S$ contains $m$, *precision* of $S$ is $m/n$

Read through Fault-Revealing tests 

#### [[Test Case Selection based on Slicing]]