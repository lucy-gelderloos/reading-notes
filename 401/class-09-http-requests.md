# Class 09 - HTTP Requests

## [Review: High-level HTTP](https://dev.to/dangolant/things-i-brushed-up-on-this-week-the-http-request-lifecycle-)

When a browser makes an HTTP request, it finds the hostname, then resolves an IP address, then checks various caches to see if the request has been made recently. If the request is not in any caches, the browser sends a DNS request containing the IP for the DNS server and the return IP address. This request is a UDP (User Data Protocol) request, so the only guaranteed response is an acknowledgment of receipt - data (like IP addresses) may not be delivered.

The request travels through various other devices & reaches the target DNS server. If that server can't find an address associated with the hostname in your request, it sends the request to another server (deference) until it reaches an "authoritative" nameserver; if it still can't find the address, the browser returns an error.

If the requesting client does receive a response, it caches it for the specified amount of time, then opens a TCP connection. Unlike UDP, TCP guarantees accurate and orderly transmission of data, so you can send a real request. To send that request, the server must be listening; the client sends a request, the server acknowledges the request, and the client acknowledges that acknowledgment.

The client can then send a request, which will have a request line, request header, and body. The body of the request is optional, and often contains data like JSON. The request follows a similar path to the previous request, but because it is using TCP, the data arrives in the same order it was sent. The server receives the request and generates a response in a similar format to the request, along with a status code describing the success (or not) of the request. As the browser receives the request, it sends acknowledgments to the server.

When the response has been received, the client sends a signal to the server; after another mutual acknowledgment, the client waits for a moment to make sure any lagging packets from other activities have arrived, then begins processing the response data.

## [Java HTTP Request Example](https://www.baeldung.com/java-http-request)

HTTPUrlRequest is a class that is part of the basic Java package and can be used to make basic HTTP requests, although it can be more cumbersome than other tools. It can create a request, add parameters and a header, configure timeouts, handle redirects, and read and build responses. There are also classes for dealing with cookies.

## Things I'd like to know more about

How Java interacts with HTTP (methods, tools, etc.).
