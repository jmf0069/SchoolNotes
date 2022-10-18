Client-Server Transaction
	-Most network applications are based on the client-server model
		-A server process and one or more of client processes
		-Server manages some resources (ex. Database)
		-Server provides service by manipulating resource for clients
	-![[Screen Shot 2022-10-12 at 12.07.10 PM.png]]
The Socket Interface
	-What is a socket?
		-A descriptor that lets an application read/write from/to the network
		-Similar abstraction for network I/O as file I/O
		-Clients and servers communicate by reading/writing from/to socket descriptors

Socket API
	-Originated with the 4.2 BSD system released in 1983
	-Sockets - A way to speak to other programs using UNIX file descriptors
	-A file descriptor is an integer associated with an open file. This can be a network connection
	-Many types of Sockets - DARPA Internet addresses (Internet Sockets), Unix Sockets, X.25 Sockets, etc
	-Types of Internet sockets
		-SOCK_STREAM uses TCP (Transmission Control Protocol)
			-Connection oriented and Reliable
		-SOCK_DGRAM uses UDP (User Datagram Protocol)
			-Connectionless and Unreliable

Internet Connections
	-Clients and servers communicate by sending streams of bytes over connections
	-Socket address is identified by an IPAddress:port pair
	-A port is a 16-bit unsigned integer identifying a process (ephemeral, not physical port)
	-Ports below 1024 are reserved for well-known services (http:80, ftp:21, ssh:22, telnet:23)
	-Ports 1024-49151 are registered ports managed by IANA
	-Dynamic/Private ports are those from 49152-65535
	-![[Screen Shot 2022-10-12 at 12.19.07 PM.png]]

Key Data Structures - IP Address
	-![[Screen Shot 2022-10-12 at 12.25.20 PM.png]]
	-32-bit IP addresses are stored in an IP address struct in <netinet/in.h>
		-IP addresses are always stored in memory in **network byte order** (big-endian byte order)
		-True in general for any integer transferred in a packet header from one machine to another
			-e.g. the port number used to identify an Internet connection
	**-Handy network byte-order conversion functions
		-htonl: convert long int from host to network byte order
		-htons: convert short int from host to network byte order
		-ntohl: convert long int from network to host byte order
		-ntohs: convert short int from network to host byte order

Byte-Ordering
	-Big-Endian (big end first) vs Little-Endian (little end first)
	-![[Screen Shot 2022-10-12 at 12.30.55 PM.png]]

IP Address Conversion Routines
	-![[Screen Shot 2022-10-12 at 12.36.24 PM.png]]
	-**inet_addr()** - Converts an IP address in numbers-and-dots notation into unsigned long
	-**inet_aton()** - Converts ascii to network address
	-**inet_ntoa()** - Returns a strong from a struct of type in_addr

Key Data Structures - Internet Socket Address
	-![[Screen Shot 2022-10-12 at 12.41.26 PM.png]]

Key Data Structures - DNS Host Entry
	-![[Screen Shot 2022-10-12 at 12.49.27 PM.png]]