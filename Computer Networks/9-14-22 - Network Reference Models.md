Network Reference Models
	-Internet TCP/IP Protocol Suite vs ISO OSI (Open System Interconnection)

TCP/IP Architecture Layers (from top to bottom):
	-App Layer
	-Transport Layer
	-Network Layer
	-Link Layer
	-Physical Layer

ISO OSI Architecture Layers (top to bottom):
	-App Layer
	-Presentation Layer
	-Session Layer
	-Transport Layer
	-Network Layer
	-Link Layer
	-Physical Layer

Internet Protocol Stack
	-Application Layer
		-Supporting network applications
		-FTP, SMTP, HTTP
	-Transport Layer
		-Process-process data transfer
		-TCP, UDP
	-Network Layer
		-Routing of datagrams from source to destination
		-IP, routing protocols
	-Link Layer
		-Data transfer between neighboring network elements
		-Ethernet, 802.11 (WiFi), PPP
	-Physical Layer
		-Bits "on the wire"

ISO/OSI Reference Model
	-Presentation Layer
		-Allow applications to interpret meaning of data. 
			-Encryption, compression, machine-specific conventions
	-Session Layer
		-Synchronization, checkpointing, recovery of data exchange
	-IP Stack does not have these layers
		-Must be implemented if needed in an application
	-Network Layer
		-Reliability
		-Congestion Control
		-Flow Control
		-Connection Setup
		-Very complex layer

-Internetworking on TCP/IP Network Layer
	- Simpler, minimal functions, autonomy
	- No reliablility / congestion control
	-Reliability is placed in the Transport Layer
		-Reliability
		-Congestion Control
		-Flow Control
		-Connection Setup

Encapsulation
	-![[Screen Shot 2022-09-14 at 12.33.47 PM.png]]
	-Application layer sends message, adds segment
	-Network layer adds header (datagram)
	-![[Screen Shot 2022-09-14 at 12.36.00 PM.png]]
	-Switch uses MAC Address to transfer frame to correct router