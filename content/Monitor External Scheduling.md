*External Scheduling* is when scheduling tasks outside the monitor is accomplished with the `_Accept` statement.

The `_Accept` statement controls which mutex members can accept calls and we can control the scheduling of tasks by preventing certain members from accepting calls at different times. 

![[Pasted image 20241208120114.png]]

![[Pasted image 20241208120449.png]]

If the accepted task does an accept, it blocks, forming a stack of blocked acceptors.


The reason *external scheduling* is simple because the actual unblocking (signalling) mechanism is *implicit*.
