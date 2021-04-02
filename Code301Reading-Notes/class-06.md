# An Introduction to Node.js on sitepoint.com
## What Is Node.js?
* Node.js® is a JavaScript runtime built on Chrome’s V8 JavaScript engine.
* Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library.
## Node Is Built on Google Chrome’s V8 JavaScript Engine
* The V8 engine is the open-source JavaScript engine that runs in Google Chrome and other Chromium-based web browsers, including Brave, Opera, and Vivaldi.
* Node.js is a program we can use to execute JavaScript on our computers. In other words, it’s a JavaScript runtime.
## How Do I Install Node.js?
* head to the official Node download page and grab the Node binaries for your system. or you use a version manager instead.
* You can check that Node is installed on your system by opening a terminal and typing node -v
## Introducing npm, the JavaScript Package Manager
*  Node comes bundled with a package manager called npm. To check which version you have installed on your system, type npm -v.
## Installing a Package Globally
`npm install -g jshint` :This will install the jshint package globally on your system.
## What Is Node.js Used For?
### Node.js Lets Us Run JavaScript on the Server
Node.js is single-threaded. It’s also event-driven, which means that everything that happens in Node is in reaction to an event. For example, when a new request comes in (one kind of event) the server will start processing it. If it then encounters a blocking I/O operation, instead of waiting for this to complete, it will register a callback before continuing to process the next event.
Node’s execution model causes the server very little overhead, and consequently it’s capable of handling a large number of simultaneous connections. The traditional approach to scaling a Node app is to clone it and have the cloned instances share the workload. Node.js even has a built-in module to help you implement a cloning strategy on a single server.
![1](https://uploads.sitepoint.com/wp-content/uploads/2012/10/1516152673node_event_loop.png)
### Are There Any Downsides?
blocking I/O calls should be avoided, CPU-intensive operations should be handed off to a worker thread, and errors should always be handled correctly for fear of crashing the entire process.
## What Kind of Apps Is Node.js Suited To?
* Node is particularly suited to building applications that require some form of real-time interaction or collaboration — for example, chat sites
* It’s also a good fit for building APIs where you’re handling lots of requests that are I/O driven 
* or for sites involving data streaming, as Node makes it possible to process files while they’re still being uploaded
## What Are the Advantages of Node.js?
speed and scalability and You can do everything in the same language, which, as a developer, makes you more productive
JavaScript is ubiquitous: most of us are familiar with JavaScript, or have used it at some point.

