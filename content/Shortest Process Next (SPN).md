The *shortest process next* is a *non-preemptive* scheduling policy where the next process is decided based on the shortest processing time ($s$) . 

It's hard to know the *processing time* $s$ for each process so we would need to make a calculation 
$$S_{n+1} = \frac{1}{n}T_{n} + \frac{n-1}{n}S_n$$
The issue with *SPN* is the possibility of *starvation* for the long-processes. This is possible if we have a constant flurry of short processes 😭

*SPN* does reduce the bias present in [[First Come First Served (FCFS)]] but is not fully viable due to the possibility of starvation and overhead with processing time calculation. 