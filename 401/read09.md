# Read: 09 - WRRC and Java


## Review: High-level HTTP

HTTP Request Lifecycle shown below:

**Local Processing**
Browser will go through its own cache of recently accessed URLs, the operating system's cache of recent queries, router's cache, and DNS cache to extract the "scheme"/protocol, host, optional port number, resource path, and query strings that are given in the form.
1. Your browser extracts the "scheme"/protocol.
2. the browser has the intended hostname for the request and the browser will look through its own cache of recently requested URLs, the operating system’s cache of recent queries, your router’s cache, and your DNS cache.

**Resolve an IP**
If the cache lookup fails, the browser sends a UDP3 DNS request to its target DNS server.
If the DNS server you have targeted cannot locate the given hostname, it passes the request along to another DNS server it is configured to defer to.\
We will assume the request is successful though, given that all of this is still a precursor. 

**Establish a TCP Connection**
Before the server can accept a three-way handshake, the client must first create a TCP connection. The server must be listening on a port and executing a passive open, after which the client can conduct an active open and the client-server connection will be recognized. This allows the receiver to restore the original order of received packets and the sender to restore the original order of sent packets. direction of communication (client->server, server->client)

**Send an HTTP Request**
A request is submitted, consisting of a "request line," a request header, and a body, and it passes through a routing mechanism.
The server receives the request, analyzes it, and locates the requested resource before returning an HTTP response.
The server generates a response and responds to the request.

**Tearing Down and Cleaning Up**
After receiving the response, the client sends a TCP FIN packet, to which the server answers with an ACK, and then sends its own FIN, to which the client responds with its own ACK signal. Then there will be a timeout. The four-way handshake is what it's called.
The browser begins to process the information it has received and then exits.

![TCP/IP](https://lh3.googleusercontent.com/proxy/WkYuLl1-Oea81n3xrLhPL1Q3fbttJgbUWQy0f1YeJZQ6MLB_Y0p2Wm7AYghCSp9HAzov14F541PAe87bazAoXNDecJOhiPO_a6yXaA)

## Do a Simple HTTP Request in Java

The **HttpUrlConnection** class allows basic HTTP queries to be made without the use of any extra libraries, and the classes we require are included in the java.net package. 
Set the **requestMethod** property to one of the following values for all sorts of requests: GET, POST, HEAD, OPTIONS, PUT, DELETE, TRACE.

To create request method follow the below steps:

**Add Request Parameters**
Set the doOutput attribute to true to add parameters to a request, then write a String of the type param1=valuem2=value to the HttpUrlConnection instance's OutputStream.

**Setting Request Headers**
To add headers to a request, use the setRequestProperty() function.
To get the value of a header field from a connection, use the getHeaderField() function.

**Configuring Timeouts**
The HttpUrlConnection class allows you to configure connect and read timeouts, which determine how long you have to wait for the server to establish a connection or for data to become available for reading. To set the timeout values, use the etConnectTimeout() and setReadTimeout() methods.

**Handling Cookies**
CookieManager and HttpCookie are two classes in the java.net package that read cookies from a response, add them to the cookie store, and ultimately add the cookies to the request.

**Handling Redirects**
Use the setInstanceFollowRedirects() function with the true or false parameter to enable or disable automatically following redirects for a given connection.
It is possible to turn on or off automatic redirection for all connections.

**Reading the Response**
Use the getResponseCode(), connect(), getInputStream(), or getOutputStream() methods to parse the HttpUrlConnection instance's InputStream, and then use the getResponseCode(), connect(), getInputStream(), or getOutputStream() methods to execute it.
The disconnect() function is used to terminate the connection.

**Reading the Response on Failed Requests**
Using HttpUrlConnection, consume the unsuccessful stream. getErrorStream().

**Building the Full Response**
Include the status of the response.
getHeaderFields returns the headers ().
Read the content of the answer and add it to the document.

![HTTP Request Lifecycle](https://miro.medium.com/max/724/1*CO8_GWJAJKjcroqYqusb0g.png)
