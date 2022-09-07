**Packet Switching: Queueing Delay, Loss**
	![[Screen Shot 2022-09-02 at 12.08.17 PM.png]]
	-Packet Queueing and loss
		-If arrival rate (in bits) to link exceeds transmission rate of link for a period of time
			-Packets will queue, wait to be transmitted on link
			-Packets can be dropped (lost) if memory (buffer) fills up

**Two Key Network-Core Functions**
	-Forwarding
		-Local action: Move arriving packets from router's input linke to appropraite router output link
	-Routing
		-Global action: Determine source-destination paths taken by packets
		-Routing algorithms
			-Creates the local forwarding table
	![[Screen Shot 2022-09-02 at 12.12.25 PM.png]]

**Circuit Switching**
	-End-end resources allocated to, reserve for "Call" between source and destination
	![[Screen Shot 2022-09-02 at 12.17.37 PM.png]]
	-In diagram, each link has four circuits
		-Call gets 2nd circuit in top link and 1st circuit in right link
	-Dedicated resources: no sharing
		-Circuit-like (guaranteed) preformance
	-Circuit segment idle if not used by call (no sharing)
	-Commonly used in traditional telephone networks

**Circuit Switching: FDM versus TDM**
	![[Screen Shot 2022-09-02 at 12.29.49 PM.png]]
	-Frequency Division Multiplexing (FDM)
		-Optical, electromagnetic frequencies divided into narrow frequency bands
		-Each call allocated its own band, can transmit at max rate of that narrow band
	-Time Division Multiplexing (TDM)
		-Time divided into slots
		-Each call allocated periodic slot(s), can transmit at maximum rate of (wider) frequency band, but only during its time slot(s)

**Packet Switching vs Circuit Switching**
	*Packet Switching Allows more Users to Use Network*
	![[Screen Shot 2022-09-02 at 12.31.53 PM.png]]
	Calculation for above:
		![[Screen Shot 2022-09-02 at 12.40.58 PM.png]]
	n = 60 users?
	Answer: Yes, the network can support 60 users using packet-switching
	![[Screen Shot 2022-09-02 at 12.42.50 PM.png]]
	n = 100 users?
	Answer: No, the network cannot support 100 users using packet-switching
	![[Screen Shot 2022-09-02 at 12.44.10 PM.png]]
	How do you know when the network stops supporting N users?
		-When there is greater than a 5% chance that more than 10 users will be on network at the same time

Is packet switching a "slam dunk winner"
	-Great for bursty data - sometimes has data to send, but at other times not
		-Resource sharing
		-Simpler, no call setup
	-Excessive congestion possible: packet delay and loss due to buffer overflow
		-Protocols needed for reliable data transfer, congestion control
	-How to provide circuit-like behavior
		-Bandwidth guarantees used for audio/video applications

Bursty Traffic
	-Use packet switching
	-Computer traffic, web access, downloads, etc
	-On-demand allocation of resources
Constant Bitrate Traffic
	-Use circuit switching
	-Resources are reserved
![[Screen Shot 2022-09-07 at 12.12.30 PM.png]]
