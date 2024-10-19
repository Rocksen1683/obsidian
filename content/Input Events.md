## Event Driven Programming 
Event-driven programming is a programming paradigm that bases program execution flow on *events*. These can represent user actions or other system actions 

## Event Types 
![[Pasted image 20240228125759.png]]
## Event Architecture 
![[Pasted image 20240228125840.png]]
![[Pasted image 20240228125910.png]]

The OS *polls* device to get current state (typically every 8ms)

## Event Creation
![[Pasted image 20240228130333.png]]

## Event Translation 
Converts *lower-level events* to *higher-level events* for programmers convenience. 
*Higher-level events* can be modelled as a state machine 

### Mouse Click State Machine 
A mouse down followed by a mouse up within a short time and with little movement is a *mouse button click*
![[Pasted image 20240228131421.png]]

### Double Click State Machine 
A click followed by another click with a short time is a *double click*
![[Pasted image 20240228131536.png]]

### Mouse Drag State Machine 
The drag start event is sent when the mouse button is held down and the mouse moves more than a small amount. Once in the dragging state, each mouse move triggers another drag event. mouse up from dragging state also sends a drag end event. 
![[Pasted image 20240228132536.png]]
### Long Press State Machine 
A mouse down followed by little movement and no mouse up for a long time is a *long press*
![[Pasted image 20240228132625.png]]

### Coalesce Frequent Events 
Main types of fundamental and translated events 
- **Discrete State Changes**: mouse up, mouse down not in high frequency and each state transition is important 
- **Continuing State Changes:** generated at high frequency and toolkit may not be able to consume them as quickly as generated 

Multiple events described in a continuous state can be *coalesced* 
-> remove or combine intermediate events since last update 


