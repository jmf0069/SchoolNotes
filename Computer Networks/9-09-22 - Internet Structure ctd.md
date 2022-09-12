Real Internet delays and routes

Compare metrics:

*Traceroute* program
	-Provides delay measurement from source to router along end-to-end Internet path towards destination
	-For all *i*:
		-Sends three packets that will reach router i on path towards destination (with time-to-live field value of i)
		-Router i will return packets to sender
		-Sender measures times interval between transmission and reply
	-Example:
		-![[Screen Shot 2022-09-09 at 12.19.53 PM.png]]

Packet Loss
	-Queue (aka buffer) preceding link in buffer has finite capacity
	-Packet arriving to full queue dropped (aka lost)
	-Lost packet may be retransmitted by previous node, by source and system, or not at all
	-![[Screen Shot 2022-09-09 at 12.23.11 PM.png]]

Throughput
	-Rate (bits/time unit) at which bits transferred between sender/receiver
		-Instantaneous: Rate at given point in time
		-Average: Rate over longer period of time
	-![[Screen Shot 2022-09-09 at 12.25.16 PM.png]]
	-![[Screen Shot 2022-09-09 at 12.28.29 PM.png]]
		-Rs
	-![[Screen Shot 2022-09-09 at 12.30.58 PM.png]]
		-Rc
	-Bottleneck Link
		-Link on end-to-end path that constrains end-to-end throughput
	-![[Screen Shot 2022-09-09 at 12.37.55 PM.png]]
	-![[Screen Shot 2022-09-09 at 12.40.32 PM.png]]

Throughput: Internet Scenario
	-![[Screen Shot 2022-09-09 at 12.42.51 PM.png]]
	-Per-connection end-end throughput: min(Rc, Rs, R/10)
	-In practice: Rc or Rs is often bottleneck

-----

