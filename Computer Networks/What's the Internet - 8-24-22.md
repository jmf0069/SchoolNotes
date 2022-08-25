What's the Internet: A "Service" View

-Infrastructure that provides services to applications
	-Web, streaming video, multimedia, games, email, etc
-Provides programming interface to apps
	-Hooks that allow sending and receiving app programs to "connect" to, use Internet transport service
	-Provides service options, analogous to postal service

------

What is a Protocol?

-Human Protocols
	-"What's the time?"
	-"I have a question"
	-Introductions

-Network Protocols
	-Machines rather than humans
	-All communication activity in Internet governed by protocols

-Protocols define format, order of messages sent, and received among network entities, and actions taken on msg transmission, receipt
-Specific Messages sent
-Specific actions taken when messages received, or other events

![[Screen Shot 2022-08-24 at 12.19.51 PM.png]]

-----

Internet Structure

Network Edge
	-Hosts: Clients and Servers
	-Servers often in data centers

![[Screen Shot 2022-08-24 at 12.24.26 PM.png]]

Access Networks, Physical Media
	-Wired, wireless communication links

![[Screen Shot 2022-08-24 at 12.25.11 PM.png]]

Network Core
	-Interconnected routers
	-Network of networks

![[Screen Shot 2022-08-24 at 12.25.42 PM.png]]

------

Access Networks and Physical Media

How to connect end systems to edge router?
	-Residential access networks
	-Institutional access networks
	-Mobile access networks
*keep in mind:*
	-Bandwidth (bits/s) of access network?
	-Shared or dedicated

![[Screen Shot 2022-08-24 at 12.28.17 PM.png]]

**Access Network: Digital Subscriber Line (DSL)**

![[Screen Shot 2022-08-24 at 12.31.14 PM.png]]

-Voice and data are transmitted at different frequencies over dedicated line from the splitter to central office

-Use *existing* telephone line to central office DSLAM
	-Data over DSL phone line goes to Internet
	-Voice over DSL phone line goes to telephone network
-24-52 Mbps dedicated downstream transmission rate
-3.5-16 Mbps dedicated upstream transmission rate
-Why is down higher than up
	-Downstream is normally what users use the most, upstream is used less often

**Access Network: Cable Network**

![[Screen Shot 2022-08-24 at 12.37.51 PM.png]]

Data and TV transmitted at different frequencies over **shared** cable distribution network

![[Screen Shot 2022-08-24 at 12.39.04 PM.png]]

**Frequency Division Multiplexing:** Different channels transmitted in different frequency bands

HFC (Hybrid Fiber Coax)
	-Asymmetric: up to 40 Mbps - 1.2 Gbs downstream transmission rate, 30-100 Mbps upstream transmission rate

Network of cable, fiber attaches homes to ISP router
	-Homes share access network to cable headend
	-Unlike DSL, which has dedicated central office

**Access Network: Home Network**

![[Screen Shot 2022-08-24 at 12.42.46 PM.png]]

Firewall
	-Software/security that prevents connections or messages that could be malicious by blocking IP address

NAT (Network Address Translation)
	-Changes local IP address so that the outside network does not see it. Allows local devices to connect to router without needing a real IP address

![[Screen Shot 2022-08-24 at 12.47.52 PM.png]]

**Wireless Access Networks**

Shared wireless access network connects end system to router
	-via base station aka "access point"

Wireless local area networks (WLANs):
	-Typically within or around building (~100ft)
	-802.1 1 b/g/n (WiFi): 11, 54, 450 Mbps transmission rate

Wide-area wireless access
	-provided by mobile cellular network operator, 10's of km away
	-10 Mbps
	-4G, LTE, 5G cellular networks

![[Screen Shot 2022-08-24 at 12.49.31 PM.png]]