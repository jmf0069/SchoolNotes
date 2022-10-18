HTTP
	-![[Screen Shot 2022-09-26 at 12.29.05 PM.png]]

Uploading Form input
	-POST Method
		-Web page often includes form input
		-User input sent from client to server in entity body of HTTP POST request message
	-URL Method
		-Uses GET method (for sending data to server)
		-Include user data in URL field of HTTP GET request message (followed by a "?")

Method Types
	-HTTP/1.0
		-GET
		-POST
		-HEAD
			-Requests headers only that would be returned if specified URL were requested with an HTTP GET method (server leave requested object out of response)
			-Useful for web caches
	-![[Screen Shot 2022-09-26 at 12.41.05 PM.png]]
	-HTTP/1.1
		-GET, POST, HEAD
		-PUT
			-Uploads new file (object) to server
			-Completely replaces file that exists at specified URL with content in entity body of POST HTTP request message
		-DELETE
			-Deletes file specified in the URL field

HTTP Response Status Codes
	-![[Screen Shot 2022-09-26 at 12.43.48 PM.png]]
	-Status code appears in 1st line in server-to-client response message
	-Some examples
		-200 OK
			-Request succeeded, requested object later in this msg
		-301 Moved Permanently
			-Requested object moved, new location specified later in this msg
		-400 Bad Request
			-Request msg not understood by server
		-404 Not Found
			-Requested document not found on this server
		-505 HTTP version not supported

Maintaining user-server state: cookies
	-No notion of multi-step exchanges of HTTP messages to complete a Web "transaction"
		-


------

