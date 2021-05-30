## Review, Research, and Discussion
* What is the benefit of transforming data into packets?
    * Packets are intended to transfer data reliably and efficiently. Instead of transferring a large file as a single block of data, sending smaller packets helps ensure each section is transmitted successfully.
* UDP is often refereed to as a connectionless protocol. Why is this?
    * UDP doesn't establish a connection between the source and destination before sending data, it just sends .
* Can a socket server application have multiple socket connections?
    yes, it can .
* Can a socket connection application be connected to multiple socket servers?
    * Yes, each listening (bound) port is serviced by a separate socket (as are all the connections made from each listening port).
* Can an application be both a socket server and a socket connection?
    * if you want to use a client socket and a server socket within a single application, then yes! You can do that if you're willing to use two different ports. Or if the sockets won't be using the same port at the same time.
## Document the following Vocabulary Terms
* Observer Pattern
    * is a software design pattern in which an object, called the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods. 
* Listener
    * An event listener is a procedure in JavaScript that waits for an event to occur.
* Event Handler
    * scripts that are automatically executed when an event occurs.
* Event Driven Programming
    * A programming paradigm where the process flow is dictated by event listeners and their handlers.
* Event Loop
    * event loop continuously checks the call stack to see if there's any function that needs to run
* Event Queue
    * is responsible for sending new functions to the track for processing.
* Call Stack
    * A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function
* Emit/Raise/Trigger
    * All these three mean firing the event, which is telling the event listener that the event is fired, then the listener activates the handler.
* Subscribe
    * enrolling in a service or agreeing to receive continuous info from a publisher, the user should input their emails or some credentials to become subscribed.
* database
    * any collection of data, or information, that is specially organized for rapid search and retrieval by a computer. Databases are structured to facilitate the storage, retrieval, modification, and deletion of data in conjunction with various data-processing operations.
## Preparation Materials
### WebSocket
WebSocket is a computer communications protocol, providing full-duplex communication channels over a single TCP connection
<br>
WebSocket is distinct from HTTP. Both protocols are located at layer 7 in the OSI model and depend on TCP at layer 4. Although they are different, RFC 6455 states
<br>
The WebSocket protocol enables interaction between a web browser (or other client application) and a web server with lower overhead than half-duplex alternatives such as HTTP polling, facilitating real-time data transfer from and to the server.
<br>
The communications are usually done over TCP port number 443 (or 80 in the case of unsecured connections), which is beneficial for environments that block non-web Internet connections using a firewall. 

### Difference Between WebSocket and Socket.io
* WebSocket is the communication Protocol that provides bidirectional communication between the Client and the Server over a TCP connection;
* WebSocket remains open all the time, so they allow real-time data transfer. When clients trigger the request to the server, it does not close the connection on receiving the response; it rather persists and waits for the Client or server to terminate the request.
* Socket.IO is a library that enables real-time and full-duplex communication between the Client and the Web servers.
* It uses the WebSocket protocol to provide the interface. Generally, it is divided into two parts; both WebSocket vs Socket.io are event-driven libraries.
#### WebSocket 
Key features of WebSocket 

* WebSocket helps in real-time communication between the Client and the webserver.
* This protocol helps in transforming to cross-platform in a real-time world between the server and the client.
* This also enables the business worldwide for a real-time web application to enhance and increase the feasibility.
* The major advantage it stands over an HTTP connection that it provides full-duplex communication.
#### Socket.IO
Key features of Socket.IO
* It helps in broadcasting to multiple sockets at a time and handles the connection transparently.
* It works on all platform, server or device, ensuring equality, reliability, and speed.
* It automatically upgrades the requirement to WebSocket if needed.
* It is a custom real-time transport protocol implementation on top of other protocols.
* It requires both libraries to be used Client side as well as a server-side library.
* IO works on work-based events. there are some reserved events that can be accessed using the Socket on the server side like Connect, message, Disconnect, Ping and Reconnect.
* There are some Client based reserved events like Connect, connect- error, connect-timeout and Reconnect etc.

Why do we need Socket.IO:
* I handle all the degradation of your technical alternatives to get full-duplex communication in real-time.
* It also handles the various support level and the inconsistencies from the browser.
* It also gives the additional feature room support for basic publish infrastructure and thinks like automatic reconnect.
* Currently, AFAIK is the most used one and easier to help with vanilla web sockets.
*** 
videos :
[OSI Model Explained](https://www.youtube.com/watch?v=vv4y_uOneC0)
<br>

[TCP Handshakes Explained](https://www.youtube.com/watch?v=xMtP5ZB3wSk)