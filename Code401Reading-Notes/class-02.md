# express 

## What’s the difference between PUT and PATCH?
The main difference between the `PUT` and `PATCH` method is that the `PUT` method uses the request URI to supply a modified version of the requested resource which replaces the original version of the resource, whereas the `PATCH` method supplies a set of instructions to modify the resource. If the `PATCH` document is larger than the size of the new version of the resource sent by the `PUT` method then the `PUT` method is preferred
## Provide links to 3 services or tools that allow you to “mock” an API for development like json-server. 
* [ Nock](https://github.com/nock/nock)
* [Postman Mock Server](https://learning.postman.com/docs/designing-and-developing-your-api/mocking-data/setting-up-mock/)
* [Wiremock](http://wiremock.org/)

## Compare and contrast Swagger and APIDoc.js 1 Which HTTP status codes should be sent with each type of (un)successful API call?
apiDocjs: Inline Documentation for RESTful web APIs. It creates a documentation from API annotations in your source code. It includes a default template which uses handlebars, Bootstrap, RequireJS and jQuery for the output of the generated apidata.js and apiproject.js as a html-page <br>
Swagger Inspector: Test and Document Your APIs With Ease. It is a free cloud-based API testing and documentation tool to simplify the validation of any API and generate its corresponding OpenAPI documentation.
* Informational responses (100–199)
* Successful responses (200–299)
* Redirects (300–399)
* Client errors (400–499)
* Server errors (500–599)

## Compare and contrast SOAP and ReST
* **`SOAP`** stands for Simple Object Access Protocol whereas **`REST`** stands for Representational State Transfer.
* **`SOAP`** is a protocol whereas **`REST`** is an architectural pattern.
* **`SOAP`** uses service interfaces to expose its functionality to client applications while **`REST`** uses Uniform Service locators to access to the components on the hardware device.
* **`SOAP`** needs more bandwidth for its usage whereas **`REST`** doesn’t need much bandwidth.
* **`SOAP`** only works with XML formats whereas **`REST`** work with plain text, XML, HTML and JSON.
* **`SOAP`** cannot make use of **`REST`** whereas **`REST`** can make use of **`SOAP`**.

***
## Express/Node introduction
### Node (or more formally Node.js) 
is an open-source, cross-platform runtime environment that allows developers to create all kinds of server-side tools and applications in JavaScript. The runtime is intended for use outside of a browser context
### Web Frameworks
A web server is a program that manages the content of a website. It's a computer software that requisitions web sites and distributes them. The web server's primary goal is to store, process, and distribute web pages to customers. The Hypertext Transfer Protocol (HTTP) is used to do this.
### Express 
is a Node. js backend web server platform distributed under the MIT License as free and open-source software. It is intended for the creation of web apps and APIs. It's been dubbed the "de facto" cloud platform for Node.js.
### Using asynchronous APIs
JavaScript code frequently uses asynchronous rather than synchronous APIs for operations that may take some time to complete. A synchronous API is one in which each operation must complete before the next operation can start.
### Routing :
refers to determining how an application responds to a client request to a particular endpoint, which is a URI (or path) and a specific HTTP request method (GET, POST, and so on).
### WRRC :
The web is a cycle of requests and responses that flow between clients and servers.
*** 
## About npm
npm is the world's largest software registry. Open source developers from every continent use npm to share and borrow packages, and many organizations use npm to manage private development as well.
### consists : 
* the website
* the Command Line Interface (CLI)
* the registry
### Use npm to :
* Adapt packages of code for your apps, or incorporate packages as they are.
* Download standalone tools you can use right away.
* Run packages without downloading using npx.
* Share code with any npm user, anywhere.
* Restrict code to specific developers.
* Create organizations to coordinate package maintenance, coding, and developers.
* Form virtual teams by using organizations.
* Manage multiple versions of code and code dependencies.
* Update applications easily when underlying code is updated.
* Discover multiple ways to solve the same puzzle.
* Find other developers who are working on similar problems and projects.
*** 
## TDD 
### Definition
“Test-driven development” refers to a style of programming in which three activities are tightly interwoven: coding, testing (in the form of writing unit tests) and design (in the form of refactoring).
### rules :
* write a “single” unit test describing an aspect of the program
* run the test, which should fail because the program lacks that feature
* write “just enough” code, the simplest possible, to make the test pass
* “refactor” the code until it conforms to the simplicity criteria
* repeat, “accumulating” unit tests over time
### Expected Benefits
* many teams report significant reductions in defect rates, at the cost of a moderate increase in initial development effort
* the same teams tend to report that these overheads are more than offset by a reduction in effort in projects’ final phases
* although empirical research has so far failed to confirm this, veteran practitioners report that TDD leads to improved design qualities in the code, and more generally a higher degree of “internal” or technical quality, for instance improving the metrics of cohesion and coupling
### Common Pitfalls
* forgetting to run tests frequently
* writing too many tests at once
* writing tests that are too large or coarse-grained
* writing overly trivial tests, for instance omitting assertions
* writing tests for trivial code, for instance accessors
***
## CI/CD :Continuous Integration Continuous Delivery
**ci :** work flow strategy that helps ensure everyone's changes and new code integrate into the current version of the software
* it helps catch bugs and reduce merge conflicts
* a team will practice ic in conjunction with an automated tester or ci server
* whenever someone introduces new code the server will test it and integrate it to the main development branch <br>

**cd :** continuous delivery 
is a process of producing a software that you could release it anytime.
continuous deployment : is an extension on continuous delivery that deploys the software at any time needed.
**webhooks :** tool used by github to send messages and communicate to external systems about activity in your project 
like when someone pushes code or make a pull request .


