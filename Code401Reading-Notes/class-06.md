# Authentication
## Review, Research, and Discussion
1. Explain what a “Singleton” is (in Computer Science terms)
    * The Singleton Pattern limits the number of instances of a particular object to just one. This single instance is called the singleton.
    * Singletons reduce the need for global variables 
* Explain how the Singleton pattern can be used with Node modules, specifically with classes 
    * A singleton is a class that allows only a single instance of itself to be created and gives access to that created instance
    * It contains static variables that can accommodate unique and private instances of itself.
    * We use it in scenarios when a user wants to restrict instantiation of a class to only one object
    * is helpful usually when a single object is required to coordinate actions across a system.
* If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?
    <!-- * create function that has access to the request object (req), the response object (res), and the next function in the application’s request-response cycle. The next function is a function in the Express router which, when invoked, executes the middleware succeeding the current middleware. -->
## Document the following Vocabulary Terms
* Router Middleware
    * Is a function that takes a request and send it to a function that handle it and eventually send a response to the client on the behalf of the original handler.
* Dynamic Module Loading
    * it is a mechanism by which a computer program can, at run time, load a library (or other binary) into memory, retrieve the addresses of functions and variables contained in the library, execute those functions or access those variables, and unload the library from memory.
* Singleton Pattern
    * it is a software design pattern that restricts the instantiation of a class to one "single" instance. 
    * it is useful when exactly one object is needed to coordinate actions across the system.
* CRUD -> REST Method Matches :
    * CREATE ---> post 
    * READ ---> get
    * UPDATE ---> put 
    * DELETE ---> delete
* Mock Testing
    *  unit testing that lets you make assertions about how the code under test is interacting with other system modules. In mock testing, the dependencies are replaced with objects that simulate the behavior of the real ones. 
## [Securing Passwords](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html)
### Brute Force attack
Hashes can't be reversed, so instead of reversing the hash of the password, an attacker can simply keep trying different inputs until he does not find the right now that generates the same hash value, called brute force attack.
### Hash Collision attack
Hash functions have infinite input length and a predefined output length, so there is inevitably going to be the possibility of two different inputs that produce the same output hash. MD5, SHA1, SHA2 are vulnerable to Hash Collision Attack i.e. two input strings of a hash function that produce the same hash result.
### BCrypt, IT's SLOW AND STRONG AS HELL
To overcome such issues, we need algorithms which can make the brute force attacks slower and minimize the impact. Such algorithms are PBKDF2 and BCrypt, both of these algorithms use a technique called Key Stretching.
## [Basic access authentication](https://en.wikipedia.org/wiki/Basic_access_authentication)
### Features
HTTP Basic authentication (BA) implementation is the simplest technique for enforcing access controls to web resources because it does not require cookies, session identifiers, or login pages; rather, HTTP Basic authentication uses standard fields in the HTTP header.
### Security
The BA mechanism does not provide confidentiality protection for the transmitted credentials. They are merely encoded with Base64 in transit and not encrypted or hashed in any way. Therefore, basic authentication is typically used in conjunction with HTTPS to provide confidentiality.
[OWASP auth cheatsheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)
## Authentication
is the process of verifying that an individual, entity or website is whom it claims to be. Authentication in the context of web applications is commonly performed by submitting a username or ID and one or more items of private information that only a given user should know.

## Session Management 
is a process by which a server maintains the state of an entity interacting with it. This is required for a server to remember how to react to subsequent requests throughout a transaction. Sessions are maintained on the server by a session identifier which can be passed back and forward between the client and server when transmitting and receiving requests. Sessions should be unique per user and computationally very difficult to predict. The Session Management Cheat Sheet contains further guidance on the best practices in this area.
## bcrypt docs
### Dependencies
* NodeJS
* node-gyp
* Please check the dependencies for this tool at: https://github.com/nodejs/node-gyp
* Windows users will need the options for c# and c++ installed with their visual studio instance.
* Python 2.x
* OpenSSL - This is only required to build the bcrypt project if you are using versions <= 0.7.7. Otherwise, we're using the builtin node crypto bindings for seed data (which use the same OpenSSL code paths we were, but don't have the external dependency).
### Why is async mode recommended over sync mode?
If you are using bcrypt on a simple script, using the sync mode is perfectly fine. However, if you are using bcrypt on a server, the async mode is recommended. This is because the hashing done by bcrypt is CPU intensive, so the sync version will block the event loop and prevent your application from servicing any other inbound requests or events. The async version uses a thread pool which does not block the main event loop.
### Compatibility Note
This library supports $2a$ and $2b$ prefix bcrypt hashes. $2x$ and $2y$ hashes are specific to bcrypt implementation developed for John the Ripper. In theory, they should be compatible with $2b$ prefix.

Compatibility with hashes generated by other languages is not 100% guaranteed due to difference in character encodings. However, it should not be an issue for most cases.