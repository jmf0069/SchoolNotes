How to improve HTTP Performance 
	-Cookies
		-Browser stores some user information and states
	-Web Caching
		-Browser stores copies of web objects

Web Caches (Proxy Server)
	-Goal
		-Satisfy client request without involving origin server
	-User configures browser to point to a web cache
	-Browser sends all HTTP requests to cachec
		-If object in cache: cache returns object
		-Else cache requests object from origin server, caches received object, then returns object to client
	-![[Screen Shot 2022-10-05 at 12.11.47 PM.png]]

Web Caches Ctd
	-Cache acts as both client and server
		-Server for original requesting client
		-Client to Origin server
	-Typically cache is installed by ISP (university, company, residential ISP)
	-Why Web Caching?
		-Reduce response time for client request
			-Cache is closer to client
		-Reduce traffic on an institution's access link
		-Internet is dense with caches
			-Enables "poor" content providers to effectively deliver content

Caching Example
	-![[Screen Shot 2022-10-05 at 12.21.10 PM.png]]
	-Access Link Rate: 1.54 Mbps
	-RTT from institutional router to any origin server: 2 sec
	-Web object size: 100K bits
	-Average request rate from browsers to origin servers: 15/sec
		-Average data rate to browsers: 1.50 Mbps
	-Consequences
		-LAN utilization: .0015
		-Access link utilization = .97
		-Total end-end delay = internet delay + access link delay + LAN delay = 2 sec + minutes + usecs
	-Average data rate = Avg Request Rate * Object Size
		-15 * 100000 = 1.5 Mbps
	-LAN Utilization
		-Data Rate / LAN rate = 1.5Mbps / 1 Gbps = .15% = .0015 => dqueue = usec
	-Access Link Utilization
		-Data Rate / Access Link Rate = 1.5 Mbps / 1.54 Mbps = 97% => dqueue = minutes
	-![[Screen Shot 2022-10-05 at 12.36.46 PM.png]]

Calculating Access Link Utilization, delay with cache
	-Suppose Cache hit rate is 0.4
		-40% of requests satisfied with cache
		-60% of requests satisfied at origin
	-Access Link Utilization
		-60% of requests use access link
	-Data rate to browsers over access link = 0.6 * 1.5 Mbps = .9 Mbps
		-Utilization = .9/1.54 = .58
	-Average end-end delay
		-0.6 * (delay from origin servers) + 0.4 * (delay when satisfied at cache)
		- = 0.6 (2.01) + 0.4 (~msecs) = ~1.2 secs
	-Lower average end-end delay than with 154 Mbps link (and cheaper as well)