# The Call Stack defined on MDN
## Call stack
A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc.
* When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.
* Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.
* When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.
* If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.
***
# Understanding the JavaScript Call Stack
The JavaScript engine (which is found in a hosting environment like the browser), is a single-threaded interpreter comprising of a heap and a single call stack. The browser provides web APIs like the DOM, AJAX, and Timers.
* The call stack is primarily used for function invocation (call). Since the call stack is single, function(s) execution, is done, one at a time, from top to bottom. It means the call stack is synchronous.
* The callback function is acted upon by the call stack during execution after the call back function has been pushed to the stack by the event loop.
* **a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call).**
### LIFO: 
Last In, First Out, it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns.
### Temporarily store: 
When a function is invoked (called), the function, its parameters, and variables are pushed into the call stack to form a stack frame. This stack frame is a memory location in the stack. The memory is cleared when the function returns as it is pop out of the stack.
### Manage function invocation (call):
The call stack maintains a record of the position of each stack frame. It knows the next function to be executed (and will remove it after execution). This is what makes code execution in JavaScript synchronous.
## What causes a stack overflow?
A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.
***
# JavaScript error messages
## Types of error messages
### Reference errors
a common thing when using const and let, they are hoisted like var and function but there is a time between the hoisting and being declared so when you try to access them a reference error occurs, the fact that this happens to let and const is called Temporal Dead Zone (TDZ).
### Syntax errors
this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.
> This can be solved by just fixing the syntax, in this case the object should be a JSON.
### Range errors
Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.
### Type errors
this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.
> he fix is simple, just make sure that property exists before trying to access it
## Debugging
1. the most common way its to simply `console.log()`
2. Using Node.js with Visual Studio Code you can press the debug tab and add a configuration
### Call stack
The call stack it’s better to navigate when you have names to your functions, meaning that if you use anonymous functions you will most probably have an harder time since the call stack will not show the name of the parent function.
*  to see the stack trace at any given point in your code is to just write console.trace() were you want to log it.
## Handling errors
* we usually try to catch the errors so we can fallback to a default state of our application in case of an error (this fallback can be a 404 page which is better than a page to just stop working).
* An alternative it’s to encapsulate our problematic function code with a try…catch which would make an error be thrown but this time, not “uncaught” so we can send it to a error logging to be checked later and send a fallback to the function so that our code continues without problems.
## Tools to avoid runtime errors
1. **quokka** to evaluate your code as you type
* **eslint** to make sure your style guide is consistency and it will grab you an error or two along the way and
***