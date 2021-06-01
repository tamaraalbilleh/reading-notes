## Review, Research, and Discussion
* What does it mean that web sockets are bidirectional? Why is this useful?
    * it works both ways, meaning that both parties can send and receive at the same time. (either the client or server can send a message to the other party whenever a message is available)

* Does socket.io use HTTP? Why?
    * Yes, socket use HTTP at the beginning to initialize the connection between the server and the client then after establish connection it start using TCP. Also if the TCP fall down socket io will start using HTTP.
* What happens when a client emits an event?
    * If the server is listening to that event, the server will execute the handler function for that event.
* What happens when a server emits an event?
    * All listening clients will execute the handler for that event.
* What happens if a client “misses” an event?
    * this means there are no listening to that event or the emitter accrue before the listener, i
* How can we mitigate this?
    * confirms that the client received the first emit in the first place

## Document the following Vocabulary Terms
* Socket : 
    * a socket is an endpoint of a communication between two programs running on a network. Sockets are used to create a connection between a client program and a server program.
* Web Socket
    * WebSocket is its own layer 7 protocol, similar to HTTP. WebSockets create a full-duplex connection for sending messages from client to server, or server to client at any instant. This pattern is far superior to HTTP request-response when an application requires systems to get the latest data ASAP.
* Socket.io
    * Socket.IO is a library that enables real-time, bidirectional and event-based communication between the browser and the server.
* Client
    * A client is a connection on the frontend.
* Server
    * A system that provides services to other systems in its network.
* OSI Model 
    * is a conceptual framework used to describe the functions of a networking system
* TCP Model
    * TCP/IP model (Transmission Control Protocol/Internet Protocol) is a model with four layers which is for both modelling current Internet architecture, as well as providing a set a rules that govern all forms of transmission over a network.
* TCP
    * TCP (Transmission Control Protocol) is a protocol for sending information between computers. TCP guarantees* that all the information will be sent and that it will be received in order.
* UDP
    * User Datagram Protocol: is a communications protocol that is primarily used for establishing low-latency and loss-tolerating connections between applications on the internet. It speeds up transmissions by enabling the transfer of data before an agreement is provided by the receiving party.
* Packets
    * is a small segment of a larger message. Data sent over computer networks, such as the Internet, is divided into packets. These packets are then recombined by the computer or device that receives them.

## Preparation Materials
### [Socket.io Chat Example](https://socket.io/get-started/chat/)
Sockets have traditionally been the solution around which most real-time chat systems are architected, providing a bi-directional communication channel between a client and a server.

for chat Server You will need to have node.js installed. We will be using express to simplify setup.

* Create a new folder with:

`$ mkdir socket.io-example`

`cd socket.io-example`

`npm install socket.io express`

Setup server and import required packages.

```
const app = require("express")();
const http = require("http").createServer(app);
const io = require("socket.io")(http);
```

The server root will send our index.html which we will setup shortly.

```
app.get("/", (req, res) => res.sendFile(\_\_dirname + "/index.html"));
```

Here is where we setup Socket.IO. It is listening for a ‘connection’ event and will run the provided function anytime this happens.

```
io.on("connection", function(socket) {
console.log(“socket connected”);
});
```
This will setup the server to listen on port 3000.

```
http.listen(3000, () => console.log("listening on http://localhost:3000")
```

Run the application with node index.js and open the page in your browser.
### [Rooms and Namespaces](https://socket.io/docs/v3/rooms/index.html)
A room is an arbitrary channel that sockets can join and leave.
* It can be used to broadcast events to a subset of clients
* rooms are a server-only concept (i.e. the client does not have access to the list of rooms it has joined).

#### Joining and leaving
```
io.on('connection', socket => {
  socket.join('some room');
});
```
And then simply use `to` or `in` (they are the same) when broadcasting or emitting:
```
io.to('some room').emit('some event');
```
You can emit to several rooms at the same time:
``` 
io.to('room1').to('room2').to('room3').emit('some event');
```
In that case, a union is performed: every socket that is at least in one of the rooms will get the event once (even if the socket is in two or more rooms).

You can also broadcast to a room from a given socket:
```
io.on('connection', function(socket){
  socket.to('some room').emit('some event');
});
```
* In that case, every socket in the room excluding the sender will get the event.
* To leave a channel you call leave in the same fashion as join.
#### Default room

Each Socket in Socket.IO is identified by a random, unguessable, unique identifier Socket#id. For your convenience, each socket automatically joins a room identified by its own id.
#### Sample use cases
broadcast data to each device / tab of a given user
send notifications about a given entity
#### Usage with asynchronous code
Please make sure to use io.to(...).emit(...) (or socket.to(...).emit(...)) in a synchronous manner.
```
// GOOD
const details = await fetchDetails();
io.to('room2').emit('details', details);
```

#### Disconnection
Upon disconnection, sockets leave all the channels they were part of automatically, and no special teardown is needed on your part.
* You can fetch the rooms the Socket was in by listening to the disconnecting event:
### [Socket.io Emit Cheatsheet](https://socket.io/docs/v3/emit-cheatsheet/index.html) <- view here
