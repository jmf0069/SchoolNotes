Network Core
	-Mesh of interconnected routers
	-Packet-switching: hosts break application-layer messages into packets
		-Forward packets from one router to the next, across links on path from source to destination
		-Each packet transmitted at full link capacity
	![[Screen Shot 2022-08-31 at 12.30.07 PM.png]]

Packet-switching: store-and-forward
	![[Screen Shot 2022-08-31 at 12.30.57 PM.png]]
	-Header packets contains destination
	-Transmission Delay
		-Takes L/R seconds to transmit (push out) L-bit packet into link at R bps
	-Store and Forward
		-Entire packet must arrive at router before it can be transmitted on next link
	-End-end Delay
		- =2L/R (assuming zero propagation delay)
	-One-hop Numerical Example:
		- L = 10 Kbits
		- R = 100 Mbps
		- One-hop trans delay = 0.1 msec
	EXAMPLE (3 Packets, same values as above): 
		**"Pipelining"	-> Overlapping Operations**
	![[Screen Shot 2022-08-31 at 12.44.55 PM.png]]