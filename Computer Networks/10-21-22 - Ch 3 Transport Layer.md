Transport layer is most complex layer of TCP IP because its the layer thats only implemented in end hosts.

Transport Services and Protocols
	-Provide logical communication between app processes running on different hosts
	-Transport protocols run in end system
		-Send side: Breaks app messages into segments, passes to network layer
		-RCV side: Reassembles segments into messages, passes to app layer
	-More than one transport protocol available to apps
		-Internet: TCP and UDP
	-![[Screen Shot 2022-10-21 at 12.41.50 PM.png]]

Transport vs Network Layer
	-Network Layer
		-Logical communication between hosts
	-Transport Layer
		-Logical communication between processes
			-Relies on and enhances network layer services
	-Household analogy
		-![[Screen Shot 2022-10-21 at 12.45.34 PM.png]]

Internet Transport-Layer Protocols
	-Reliable, in-order delivery (TCP)
		-Congestion Control
		-Flow Control
		-Connection Setup
	-Unreliable, unordered delivery (UDP)
		-No-frills extension of "best-effort" IP
	-Services not available:
		-Delay Guarantees
		-Bandwidth Guarantees

-----

Multiplexing / Demultiplexing
	-![[Screen Shot 2022-10-24 at 12.09.55 PM.png]]
	-Multiplexing at sender:
		-Handle data from multiple sockets, add transport header (later used for demultiplexing)
	-Demultiplexing at receiver:
		-Use header info to deliver received segments to correct socket

How Demultiplexing Works
	-Host receives IP datagrams
		-Each datagram has source IP address, destination IP address
		-Each datagram carries one transport-layer segment
		-each segment has source, destination port number
	-Host uses IP addresses and Port Numbers to direct segment to appropriate socket
	-![[Screen Shot 2022-10-24 at 12.13.19 PM.png]]

**Connectionless** Demultiplexing
	-Recall: Created socket has host-local port # : DatagramSocket mySocket1 = new DatagramSocket(12543)
	-Recall: When creating datagram to send into UDP socket, must specify:
		-Destination IP address
		-Destination Port #
	-When host receives UDP segment:
		-Checks destination port # in segment
		-Directs UDP segment to socket with that port #
	-IP datagrams with same destination port # but different source IP addresses and/or source port numbers will be directed to same socket at destination
	-![[Screen Shot 2022-10-24 at 12.24.26 PM.png]]

Connection-Oriented Demux
	-![[Screen Shot 2022-10-24 at 12.26.23 PM.png]]
	-TCP Socket identified by 4-tuple
		-Source IP address
		-Source port number
		-Destination IP address
		-Destination port number
	-Demux: Receiver uses all four values to direct segment to appropriate socket
	-Server host may support many simultaneous TCP sockets
		-Each socket identified by its own 4-tuple
	-Web servers have different sockets for each connecting client
		-Non-persistent HTTP will have different socket for each request
	-![[Screen Shot 2022-10-24 at 12.28.28 PM.png]]

------

Connectionless Transport: UDP
	-"No frills", "bare bones" Internet transport protocol
	-"Best effort" service, UDP segments may be:
		-Lost
		-Delivered out-of-order to app
	-Connectionless
		-No handshaking between UDP sender, receiver
		-Each UDP segment handled independently of others
	-UDP examples
		-Streaming multimedia apps (loss tolerant, rate sensitive)
		-DNS
		-SNMP
	-Reliable transfer over UDP
		-Add reliability at application layer
		-Application-specific error recovery

UDP: Segment Header
	-![[Screen Shot 2022-10-24 at 12.42.18 PM.png]]

UDP Checksum
	-Goal: Detect "errors" (e.g. flipped bits) in transmitted segment
	-Sender
		-Treat segment contents, including header fields, as sequence of 16-bit integers
		-Checksum: Addition (one's complement sum) of segment contents
		-Sender puts checksum value into UDP checksum field
	-Receiver
		-Compute checksum of received segment
		-Check if computed checksum equals checksum field value
			-NO - error detected
			-YES - no error detected

Internet Checksum Example
	-![[Screen Shot 2022-10-24 at 12.49.22 PM.png]]