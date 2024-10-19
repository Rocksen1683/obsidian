We know that [[Shortest Process Next (SPN)]], [[Shortest Running Time (SRT)]], [[Highest Response Ratio Next (HRRN)]] all need the calculation of the processing time $s$ which could either not be possible or would require a heavy overhead. 

To avoid this we can have a policy that *pre-emptively* chooses processes based on some feedback on how much time the process is taking. If it is taking a long time, the scheduler can penalize the process.
![[Pasted image 20240326171143.png]]
