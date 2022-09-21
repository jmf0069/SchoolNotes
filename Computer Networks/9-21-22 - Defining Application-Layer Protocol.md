An Application Layer Protocol defines:
	-Types of messages exchanged
		-e.g. request, response
	-Message Syntax
		-What fields in messages and how fields are delineated
	-Message Semantics
		-Meaning of information in fields
	-Rules for when and how processes send and respond to messages
	-**Open Protocols**
		-Defined in RFCs, everyone has access to protocol definition
		-Allows for interoperability
		-e.g. HTTP, sMTP
	-**Proprietary Protocols**
		-e.g. Skype

What transport service does an application need?
	-Data Integrity
		-Some apps (e.g. file transfer, web transactions) require 100% reliable data transfer
		-Other apps (e.g. audio) can tolerate some loss
	-Timing
		-Some apps (e.g. internet telephony, games) require low delay to be "effective"
	-Throughput
		-Some apps (e.g. multimedia) require minimum amount of throughput to be "effective"
		-Other apps ("elastic apps" such as FTP or remote shells) make use of whatever throughput they get
	-Security
		-Encryption, data integrity, etc
	-![[Screen Shot 2022-09-21 at 12.17.14 PM.png]]

Internet Transport Protocol Services
	-TCP Service
		-Reliable Transport between sender and receiver
		-Flow control
			-Send won't overwhelm receiver
		-Congestion Control
			-Throttle sender when network overloaded
		-Does not provide timing, minimum throughput guarantee, or security
		-Connection-Oriented
			-Setup required between client and server processes
	-UDP Service
		-Unreliable data transfer between sending and receiving process
		-Does not provide reliability, flow control, congestion control, timing, throughput guarantee, security, or connection setup
	-Why choose UDP?
		-Simple and easy setup
		-No setup required for any of the things not provided
		-Used for some applications that don't want to be throttled down when transmission is used (such as some multimedia services)
	-![[Screen Shot 2022-09-21 at 12.25.10 PM.png]]

Securing TCP
	-TCP and UDP
		-No Encryption
		-Cleartext passwords sent into socket traverse internet in cleartext
	-SSL
		-Provides encrypted TCP connection
		-Data integrity
		-End-point authentication
		-SSL is at application layer
			-Apps use SSL libraries which "talk" to TCP
		-SSL Socket API
			-Cleartext passwords sent into socket traverse Internet encrypted
	-![[Screen Shot 2022-09-21 at 12.27.36 PM.png]]