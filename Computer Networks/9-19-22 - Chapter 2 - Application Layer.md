Application Layer

Goals
	-Conceptual and implementation aspects of application-layer protocols
		-Transport-layer service models
		-Client-Server Paradigm
		-Peer-to-peer paradigm
	-Learn about protocols by examining popular application-level protocols
		-HTTP
		-FTP
		-SMTP / POP3 / IMAP
		-DNS
	-Creating Network Applications
		-Socket API

Creating a Network Application
	-Write programs that:
		-Run on different end systems
		-Communicate over network
		-e.g. web server software communicates with browser software
	-No need to write software for network-core devices
		-Network-core devices do not run user applications
		-Applications on end systems allows for rapid app development, propagation
	-Transport layer provides interface for systems to communicate

Client-Server Model vs Peer-to-Peer model
	-Client-Server Model
		-![[Screen Shot 2022-09-19 at 12.19.00 PM.png]]
		-Client always initiates communication (request)
		-States saved when crashes occur
			-![[Screen Shot 2022-09-19 at 12.24.25 PM.png]]
	-Peer-to-Peer Model
		-![[Screen Shot 2022-09-19 at 12.20.07 PM.png]]
		-Communication can be initiated by any peer
		-Timeline
			-![[Screen Shot 2022-09-19 at 12.27.40 PM.png]]
		-Why is P2P used?
			-Scalability
				-Any user can be the server (Peers act as both client and server) so you can pick a "server" that is closer to the user.
			-Harder to trace the origin of the transmission which makes the commmunication more secure

Client-Server Architecture
	-Server
		-Always-on host
		-Permanent IP address
		-Often in data centers, for scaling purposes
	-Clients
		-Communicate with server
		-May be intermittently connected
		-May have dynamic IP addresses (DHCP - Dynamic Host Communication Protocol)
		-Do not communicate directly with other clients
		-E.g. HTTP, IMAP, FTP

Peer-to-Peer Architecture
	-Not always-on server
	-Arbitrary end systems directly communicate
	-Peers request service from other peers, provide service in return to other peers
		-Self Scalability
			-New peers bring new service capacity, as well as new service demands
		-Peers are intermittently connected and change IP addresses
			-Complex management
		-E.g. Peer-to-Peer file sharing

Processes Communicating
	-Process
		-Program running within a host
		-Within same host, two processes communicate using inter-process communication (defined by OS)
		-Processes in different hosts communicate by exchanging messages
	-Clients and Servers
		-Client process
			-Process that initiates communication
		-Server Process
			-Process that waits to be contacted
	-Note: Applications with P2P architectures have client processes and server processes

Sockets
	-Process sends/receives messages to/from its socket
	-Socket analogous to door
		-Sending process shoves message out door
		-Sending process relies on transport infrastructure on other side of door to deliver message to socket at receiving process
	-![[Screen Shot 2022-09-19 at 12.43.53 PM.png]]
	-Unique socket for each process
		-Identified by the port number appended to the end of the IP address

Addressing Processes
	-![[Screen Shot 2022-09-19 at 12.49.52 PM.png]]