If *arrival rate* (in bps) to the link exceeds the *transmission rate* (bps) of the link then the following can happen
- packets will *queue*, waiting to be transmitted on the output link 
- packets can also be dropped (*lost*) if the buffer is full 

To help with this, we could potentially use [[Circuit Switching]] instead of [[Packet Switching]].

## Sources of Packet Loss
Here are some sources of packet loss:
1. Transmission
2. Nodal Processing 
3. Queuing 
4. Propagation

The total delay over $1$ hop is:
$$d_{1hop} = d_{proc} + d_{queue} + d_{trans} + d_{prop}$$
### Nodal Processing Delay 
The delay is mainly due to: 
- checking bit errors 
- determining output links 

Usually, the delay is smaller than microseconds. 

### Queuing Delay 
Delay occurs due to
- time waiting at the output link for transmission 
- usually depends on the congestion layer of buffer 
We can calculate it by:
- $a$: avg packet arrival rate 
- $L$: packet length (bits)
- $R$: link bandwidth 

$$d_{queue} = \frac{La}{R}$$

### Transmission Delay 
Delay occurs due to [[Packet Switching]] and is mainly calculated by 
$$d_{trans} = \frac{L}{R }$$
### Propagation Delay 
To calculate *propagation delay*, we would need 
- $d$: length of the physical link 
- $s$: propagation speed ($~ 2\times 10^{8}$ m/s)

$$d_{prop} = \frac{d}{s}$$


