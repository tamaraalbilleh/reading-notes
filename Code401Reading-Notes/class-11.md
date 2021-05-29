## Review, Research, and Discussion
* Why is access control important?
    1. INCREASE EASE OF ACCESS FOR EMPLOYEES
    2. GET RID OF TRADITIONAL KEYS
    3. KEEP TRACK OF WHO COMES AND GOES
    4. PROTECT AGAINST UNWANTED VISITORS
    5. PREVENT AGAINST DATA BREACHES 
    6. CREATE A SAFE WORK ENVIRONMENT
    7. REDUCE THEFT AND ACCIDENTS
    8. COMPLY WITH INDUSTRY REGULATIONS OR SECURITY STANDARDS
* Describe an application that would need access control.
   * maybe apps with different levels of data sensitivity 
* What is a role used for?
   * it determines which permissions the system grants to the user.
* Why is role based access control more scalable than discretionary or mandatory access control?
   * ACL is better suited for implementing security at the individual user level and for low-level data, while RBAC better serves a company-wide security system with an overseeing administrator. 
## Document the following Vocabulary Terms
* Authorization : Giving permission for a user to perform a certain action or get access to certain data .
* Role Based Access Control : A system where users have assigned roles, and permissions and capabilities are granted based on those roles.
* Capabilities : the permissions and actions specified for each role .
## [Event-Driven Programming in Node.js](https://www.digitalocean.com/community/tutorials/nodejs-event-driven-programming)
Event-Driven Programming is a logical pattern that we can choose to confine our programming within to avoid issues of complexity and collision
### Overview
* Every time you interact with a webpage through it’s user interface, an event is happening.
* These events have associated functions that, when triggered, are executed to make a change to the user interface in some way.
* Event-Driven Programming makes use of the following concepts:
   * An Event Handler is a callback function that will be called when an event is triggered.
   * A Main Loop listens for event triggers and calls the associated event handler for that event.
### EventEmitter
* Node.js natively provides us with a useful module called EventEmitter that allows us to get started incorporating Event-Driven Programming in our project 
* We access the EventEmitter class through the events module `const EventEmitter = require('events').EventEmitter;`
* Once imported we’ll need to create a new object from the class to start using it. `const myEventEmitter = new EventEmitter;`
* First, we’ll write a function that will act as our event listener
   ```
   function userJoined(username){
  // Assuming we already have a function to alert all users.
  alertAllUsers('User ' + username + ' has joined the chat.');
   }
   ```
* then we can use EventEmitters on method to set the listener.
   ```
   // Run the userJoined function when a 'userJoined' event is triggered.
   chatRoomEvents.on('userJoined', userJoined);
   ```
* EventEmitter has an emit method that we we use to trigger the event.
### [Removing Listeners](https://nodejs.org/api/events.html)
This could be for performance reasons (the event is no longer needed) or to avoid memory leaks (if an event listener references an object that is no longer needed, it won’t be able to be garbage-collected. This can lead to a build up of unnecessary objects). `chatRoomEvents.removeListener('message', displayMessage);`
* To remove event listeners in EventEmitter we can use the removeListener or removeAllListeners method.
* in the EventEmitter that comes built-in with Node you must pass a reference to the exact function you wish to remove when using the removeListener method (it is often best to name your event handling functions and declaring them before you register the event listener, as opposed to leaving them anonymous.)
### Object Oriented Programming + Event-Driven Programming
* The Object Oriented approach promotes the idea that all behavior of an individual unit (or object) be handled from code within that unit.
* By registering event listeners we can actually reverse the flow of communication between our objects
