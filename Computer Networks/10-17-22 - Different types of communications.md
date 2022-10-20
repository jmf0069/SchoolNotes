Connection-Oriented (TCP) vs Connectionless Communications (UDP)
	Connection-Oriented
		-First, connection is established between two ends
		-Then, they communicate through the connection
	Connectionless (datagram)
		-Whenever one sends message to the other, the destination address is included (
		no connection)
		-Packet could be lost or delivered out of order

Socket programming with **Connectionless Protocol**
	-![[Screen Shot 2022-10-17 at 12.11.14 PM.png]]

Socket Programming With **Connection-Oriented Protocol**
	-![[Screen Shot 2022-10-17 at 12.13.29 PM.png]]

Transmission Control Protocol
	-Allow networked computers to reliably transfer byte streams
	-Connection-oriented provides error recovery and data flow
	-Data received in correct order
	-More information on RFC793
	-![[Screen Shot 2022-10-17 at 12.17.20 PM.png]]

Client: Creating a Socket
	-![[Screen Shot 2022-10-17 at 12.20.21 PM.png]]

Server: Binding a Local Address
	-![[Screen Shot 2022-10-17 at 12.23.25 PM.png]]

Client: Obtaining a Server's Address
	-![[Screen Shot 2022-10-17 at 12.29.26 PM.png]]

-----

UDP Socket Programming

Client: Sending Datagrams
	-![[Screen Shot 2022-10-17 at 12.34.17 PM.png]]

Server: Receiving Datagrams
	-![[Screen Shot 2022-10-17 at 12.35.37 PM.png]]

DG Client Echo Processing
	-![[Screen Shot 2022-10-19 at 12.13.07 PM.png]]

UDP Echo Server
	-![[Screen Shot 2022-10-19 at 12.19.47 PM.png]]

DG Server Echo Processing
	-![[Screen Shot 2022-10-19 at 12.23.10 PM.png]]

Bare minimum UDP Client
	-![[Screen Shot 2022-10-19 at 12.26.16 PM.png]]