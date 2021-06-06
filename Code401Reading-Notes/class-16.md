## Review, Research, and Discussion
* Describe the Web-Request-Response-Cycle
    * A user opens his browser, types in a URL, and presses Enter.
    * When a user presses Enter, the browser makes a request for that URL.
    * The request hits the Rails router (config/routes.rb). The router maps the URL to the correct controller and action to handle the request.
    * The action receives the request and passes it on to the view.
    * The view renders the page as HTML.
    * The controller sends the HTML back to the browser. The page loads and the user sees it.

* Explain what a “server” is, as it relates to the WRRC
    * SERVER is simply a computer that runs all the time and deal with requests (HTTP) and responses form clients or other servers, also sending requests to the database and back to the clients with responses.
* What does it mean to “deploy” an application?
    * Software deployment is all of the activities that make a software system available for use.

## Document the following Vocabulary Terms
* Server : 
    * is a piece of computer hardware or software (computer program) that provides functionality for other programs or devices, called "clients".
* Pub/Sub : 
    * Publish/Subscribe is an interaction pattern that characterizes the exchange of messages between publishing and subscribing clients. Subscribers express interest in receiving messages and publishers simply publish messages without specifying the recipients for a message. 
* WRRC :
    * Web-Request-Response-Cycle is a cycle that show the flow of data when a user or server make request to specific site then this request will go to the ISP (internet service provider) to check the DNS (Domain name server, which is basically a lot of IP addresses) and find to you the IP address of the server you are requesting then send request to that server and that server will check this request and check the databases then back with a response to your ISP and back to you with the final results.
## Preparation Materials
### AWS EC2
Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure, resizable compute capacity in the cloud. It is designed to make web-scale cloud computing easier for developers. Amazon EC2’s simple web service interface allows you to obtain and configure capacity with minimal friction. It provides you with complete control of your computing resources and lets you run on Amazon’s proven computing environment.
### [EC2 For Humans](https://www.youtube.com/watch?v=lZMkgOMYYIg)
* Virtual Machine 
    * a virtual machine (VM) is the virtualization/emulation of a computer system. Virtual machines are based on computer architectures and provide functionality of a physical computer. Their implementations may involve specialized hardware, software, or a combination.

example :
* virtual box
* vm ware


AWS : is a web service that provides secure, resizable compute capacity in the cloud.

* It is designed to make web-scale cloud computing easier for developers.
* allows you to obtain and configure capacity with minimal friction.
* It provides you with complete control of your computing resources.
* lets you run on Amazon’s proven computing environment.
* offers the broadest and deepest compute platform with choice of processor, storage, networking, operating system, and purchase model.
##### AWS S3
* S3 stands for Amazon Simple Storage Service.
* As the name suggests, it provides storage over the internet where you can store and secure your data.
* designed to make web-scale computing easier for developers.
* It offers industry-leading scalability, data availability, security, and performance.
##### AWS Lambda:
* It is a service which computes the code without any server.
* It is an event-driven serverless compute service.
* Use mostly Node JS and Python.
### [Elastic Beanstalk](https://www.youtube.com/watch?v=SrwxAScdyT0)
easy to use service that deploys , manages and scales web apps and services
it uses managed containers that support environments such as java , .NET , PHP , Node.js , Python ,Ruby and docker on familiar servers such as apache HTTP server, apache tomcat ,nginx passenger and iis .
