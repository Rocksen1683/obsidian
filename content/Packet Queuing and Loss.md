If *arrival rate* (in bps) to the link exceeds the *transmission rate* (bps) of the link then the following can happen
- packets will *queue*, waiting to be transmitted on the output link 
- packets can also be dropped (*lost*) if the buffer is full 

To help with this, we could potentially use [[Circuit Switching]] instead of [[Packet Switching]].