### What happens when you type a URL in the browser then press enter?

When you type a web address, say google.com, into your browser address bar, the following steps occur:

### DNS request
The browser seeks to translate the domain name *www.google.com* to an IP address.

A query is sent to a DNS server, fetching the corresponding IP address for Google's server.

### The protocol suite: TCP/IP

With the IP address at hand, the protocol suite kicks in. 

TCP establishes a reliable connection between your machine and Google's server, ensuring data integrity and order. 

IP, on the other hand, is responsible for routing the data packets to the correct destination.

Before the packets venture further, they encounter a firewall that scrutinizes the packets based on predefined rules before permitting them onward. 

This ensures that only safe and authorized traffic is allowed through.

### The secure passage: HTTPS/SSL

In the secure domain (https), Secure Socket Layer (SSL) or its successor Transport Layer Security (TLS) ensure a secure connection by encrypting the data transferred between your browser and Google's server, safeguarding against eavesdropping.

HTTP headers contain additional information about the response.

A status code indicating whether the request was successful. 
|Status code | Meaning | Uses|
|--------|-------|-------|
|200 | HTTP request was successful| The resource has been fetched/ request as received by the server|
|301| Requested resource permanently moved to a new location|Renders content when moved|
|404|Server cannot find the requested resource|Returned if the URL is wrong|
|503|Request not handled due to a problem with the server|Common when servers are offline for maintenance|


Once the packets arrive, a load balancer distributes incoming network traffic across several servers to ensure no single server becomes overwhelmed with too much traffic. 

The application server executes the necessary business logic, interacting with the database and preparing the HTTP response to be sent back to your browser.

To fulfill your request, the application server might need to fetch or store data. 

It interacts with the database, where data is stored, retrieved, and managed, ensuring that your search query is successfully executed.

The HTTP response makes its way back through the channels, reaching your browser which then renders the webpage known as Google.
