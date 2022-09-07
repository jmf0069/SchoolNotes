Internet Structure: Network of Networks
	-End systems connect to Internet via access ISPs
		-Residential, enterprise (company, university, commercial) ISPs
	-Access ISPs in turn must be interconnected
		-So that any two hosts can send packets to each other
	-Resulting network of networks is very complex
		-Evolution was driven by economics and national policies

Question: How do we connect the ISPs?
	-Option: Connect each access ISP to every other access ISP
		-![[Screen Shot 2022-09-07 at 12.22.27 PM.png]]
		-CON: Does not scale well. O(N^2) connections
	-Option: Connect each access ISP to a global ISP? Customer and provider ISPs have economic agreement
		-![[Screen Shot 2022-09-07 at 12.23.59 PM.png]]
	![[Screen Shot 2022-09-07 at 12.27.32 PM.png]]

Tier-1 ISP Network Map: Sprint (2019)
	-![[Screen Shot 2022-09-07 at 12.28.48 PM.png]]

---------

How do loss and delay occur?
	-Packets queue in router buffers
		-Packets queue, wait for turn
		-Packet arrival rate to link exceeds output link capacity: packet loss
		-![[Screen Shot 2022-09-07 at 12.32.39 PM.png]]
	Four sources of packet delay
		-![[Screen Shot 2022-09-07 at 12.33.55 PM.png]]
		-d.proc: Nodal Processing
			-Check bit errors
			-Determine output link
			-Typically < 1 msec
		-d.queue: Queueing Delay
			-Time waiting at output link for transmission
			-Depends on congestion level of router
		-![[Screen Shot 2022-09-07 at 12.34.36 PM.png]]
		-d.trans: Transmission delay
			-L: packet length (bits)
			-R: link transmission rate (bps)
			-d.trans = L/R
		-d.prop: Propagation delay
			-d: length of physical link
			-s: propagation speed in medium
			-d.prop = d/s
		-![[Screen Shot 2022-09-07 at 12.37.35 PM.png]]

Caravan Analogy
	-![[Screen Shot 2022-09-07 at 12.41.23 PM.png]]
![[Screen Shot 2022-09-07 at 12.41.39 PM.png]]
![[Screen Shot 2022-09-07 at 12.42.22 PM.png]]

Packet queueing delay
	-R: link bandwidth (bps)
	-L: packet length (bits)
	-a: average packet arrival rate
	-![[Screen Shot 2022-09-07 at 12.45.29 PM.png]]
	-La/R ~ 0: Average queuing delay is small
	-La/R >= 1: Average queuing delay large
	-La/R 
	-![[Screen Shot 2022-09-07 at 12.49.55 PM.png]]
