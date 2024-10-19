Two main types of switching/forwarding in networks. 
## [[Packet Switching]]
## [[Circuit Switching]]

## [[Packet Switching]] vs [[Circuit Switching]]
Let's consider  an example with a 1 Gbps link and each user consumes 100 Mb/s when active. Each user is active around $10\%$ of the time. 

How many users can use this network simultaneously under circuit-switching and packet switching (without congestion for packet switching)?

*circuit-switching:* 10 users

*packet switching:* with M=35 users, probability > 8 active at same time is 0.0063.

So, [[Packet Switching]] will be greater for a burst of data but at other times not and is possible for *excessive congestion* due to [[Packet Queuing and Loss]].

