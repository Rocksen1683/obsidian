The *decision mode* specifies the instants in time at which the [[Selection Function for Scheduling]] is exercised

#### Non Pre-emptive
In this case, once a process is in the *Running* state, it continues to execute until: 
1. It *terminates*
2. It *blocks* itself to request some service or resource from the OS 

#### Pre-emptive
Pre-emption would  be when the current *running* process gets interrupted and moved to *ready* by the OS. This can be done when 
-  A new process arrives 
- Interrupt occurs  
- Based on a clock interrupt 

*Pre-emptive* processes incur greater overhead than non pre-emptive ones but also perform better as they don't let a particular process monopolize the usage of processor time. 