## Review, Research, and Discussion
- Name 3 real world use cases where you’d want to change the request with custom middleware
    - Authentication
    - Error Handling
    - Data Modelling
- True or false: The route handler is middleware?
    - False : They are not middleware functions by definition. If such function is used on routing methods when it is the only one callback function then they are only handler functions.there is no need for next which calls the next middleware function and makes it a middleware.

- In what ways can a middleware function end the process and send data to the browser?
    - when there is an error thrown when calling them .
- At what point in the request lifecycle can you “inject” middleware?
    - when sending a request and before calling the handler of the route 
- What can cause express to error with “Request headers sent twice, cannot start a second response”
    - means that you’re already in the Body or Finished state, but some function tried to set a header or statusCode. When you see this error, try to look for anything that tries to send a header after some of the body has already been written
     *** 

## Document the following Vocabulary Terms
* Middleware 
    - functions that have access to the request object (req), the response object (res), and the next function (function in the Express router which, when invoked, executes the middleware succeeding the current middleware) in the application’s request-response cycle.
* Request Object
    - an object of all the info sent through http requests from clients to server . 
* Response Object
    - an object of the info sent through http responses from the server to the client.
* Application Middleware
    - Middleware that plays a role in the function of the application.
* Routing Middleware
    - Middleware that plays a role in path routing.
* Test Driven Development
    - is software development approach in which test cases are developed to specify and validate what the code will do
* Behavioral Testing
    - Behavioral Testing is a testing of the external behavior of the program, also known as black box testing. It is usually a functional testing.
    ***
## Preparation Materials

### Review: ES6 Classes
  * Classes are a template for creating objects.
  * Classes are in fact "special functions"
#### Defining classes
> the class syntax has two components:
1.  class expressions
2.  class declarations
##### Class declarations

```
class className {
  constructor(param1, param2) {
    this.param1 = param1;
    this.param2 = param2;
  }
}

```
> An important difference between `function declarations` and `class declarations` is that `function declarations` are hoisted and c`lass declarations` are not.
*  You first need to declare your class 
*  then access it<br>
 otherwise code like the following will throw a ReferenceError:

##### Class expressions
this is another way to define a class. 
* Class expressions can be named or unnamed. 
* The name given to a named class expression is local to the class's body

```
// unnamed
let classN = class {
   constructor(param1, param2) {
    this.param1 = param1;
    this.param2 = param2;
  }
};

// named
let classN = class className {
  constructor(param1, param2) {
    this.param1 = param1;
    this.param2 = param2;
  }
};
```
### Using Express Routing ( Routing )
Routing refers to how an application’s endpoints (URIs) respond to client requests. <br>
You define routing using methods of the Express app object that correspond to HTTP methods <br>
for example : 
1. `app.get()` to handle GET requests 
2. `app.post()` to handle POST requests.
3. `app.all()` to handle all HTTP methods 
4. `app.use()` to specify middleware as the callback function <br>

the application “listens” for requests that match the specified route(s) and method(s), and when it detects a match, it calls the specified callback function.
*  routing methods can have more than one callback function as arguments. With multiple callback functions, it is important to provide next as an argument to the callback function and then call next() within the body of the function to hand off control to the next callback
#### Route paths
it defines the endpoints at which requests can be made.<br> 
Route paths can be : strings, string patterns, or regular expressions.
The characters `? + *` and `()` are subsets of their regular expression counterparts. The hyphen (`-`) and the dot (`.`) are interpreted literally by string-based paths.
If you need to use the dollar character (`$`) in a path string, enclose it escaped within (`[` and `]`)
##### Route parameters
Route parameters are named URL segments that are used to capture the values specified at their position in the URL. The captured values are populated in the req.params object, with the name of the route parameter specified in the path as their respective keys
#### Route handlers
You can provide multiple callback functions that behave like middleware to handle a request. The only exception is that these callbacks might invoke next('route') to bypass the remaining route callbacks. You can use this mechanism to impose pre-conditions on a route, then pass control to subsequent routes if there’s no reason to proceed with the current route.
***

[Express Routing](https://scotch.io/tutorials/learn-to-use-the-new-router-in-expressjs-4)
