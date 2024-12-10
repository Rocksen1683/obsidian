To control [[Principles of Congestion Control]], [[Transmission Control Protocol]] follows the following approach: 
- sender increases the transmission rate (specifically, it's window size, i.e, `cwnd`) until problem (loss event occurs)
- when problem is detected, it decreases `cwnd`
- By controlling the *window size*, TCP effectively controls the rate.
![[Pasted image 20241204182846.png]]

![[Pasted image 20241204182948.png]]
![[Pasted image 20241204182959.png]]
![[Pasted image 20241204183018.png]]
![[Pasted image 20241204183035.png]]
![[Pasted image 20241204183119.png]]
## [[TCP AIMD]]
## [[TCP CUBIC]]

![[Pasted image 20241204183554.png]]

## Delay-based TCP Congestion Control

![[Pasted image 20241204183622.png]]
![[Pasted image 20241204183628.png]]
## [[Explicit Congestion Notification]]