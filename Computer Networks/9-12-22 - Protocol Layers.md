Protocol Layers, Service Models

Protocol "Layers"
	-Networks are complex with many pieces:
		-Hosts, routers, links of media, applications, protocols, hardware, software, etc
	-Question: Is there any hope of organizing structure of network?
	-![[Screen Shot 2022-09-12 at 12.10.10 PM.png]]
	Layers: each layer implements a service
		-Via its own internal-layer actions
		-Relying on services provided by layer below

How to build/design very large complex networks?
	-Break down complex systems into smaller components
	-Module (modularization)
		-Interface
			-Well known
		-Implementation
			-Hidden
				-Makes it easier to modify/update implementation without affecting other modules
		-![[Screen Shot 2022-09-12 at 12.30.29 PM.png]]
			-Deadlock
				-Recovery via Reboot
				-Avoid via Layering!
					-![[Screen Shot 2022-09-12 at 12.37.21 PM.png]]
	-Summary: ![[Screen Shot 2022-09-12 at 12.43.37 PM.png]]

Network Reference Models
	-Internet TCP/IP Protocol Suite vs ISO OSI (Open System Interconnection)