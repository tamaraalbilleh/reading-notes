# Sending form data
## Client/server architecture
the web uses a client/server architecture : a client (usually a web browser) sends a request to a server (most of the time a web server like Apache, Nginx, IIS, Tomcat, etc.), using the HTTP protocol. The server answers the request using the same protocol.
* An HTML form on a web page is nothing more than a convenient user-friendly way to configure an HTTP request to send data to a server.
## On the client side: defining how to send the data
The `<form>` element defines how the data will be sent. All of its attributes are designed to let you configure the request to be sent when a user hits a submit button. The two most important attributes are action and method
### The action attribute
The action attribute defines where the data gets sent. Its value must be a valid relative or absolute URL. If this attribute isn't provided, the data will be sent to the URL of the page containing the form — the current page
### The method attribute
The method attribute defines how data is sent. The HTTP protocol provides several ways to perform a request; HTML form data can be transmitted via a number of different methods, the most common being the GET method and the POST method
#### The GET method
The GET method is the method used by the browser to ask the server to send back a given resource
#### The POST method
The POST method is a little different. It's the method the browser uses to talk to the server when asking for a response that takes into account the data provided in the body of the HTTP request
### Viewing HTTP requests
The only thing displayed to the user is the URL called. As we mentioned above, with a GET request the user will see the data in their URL bar, but with a POST request they won't. This can be very important for two reasons
## On the server side: retrieving the data
Whichever HTTP method you choose, the server receives a string that will be parsed in order to get the data as a list of key/value pairs. The way you access this list depends on the development platform you use and on any specific frameworks you may be using with it.
## A special case: sending files
The enctype attribute
This attribute lets you specify the value of the Content-Type HTTP header included in the request generated when the form is submitted. This header is very important because it tells the server what kind of data is being sent.
> If you want to send files, you need to take three extra steps:

* Set the method attribute to POST because file content can't be put inside URL parameters.
* Set the value of enctype to multipart/form-data because the data will be split into multiple parts, one for each file plus one for the text data included in the form body (if text is also entered into the form).
* Include one or more `<input type="file">` controls to allow your users to select the file(s) that will be uploaded.
## Security issues
Each time you send data to a server, you need to consider security. HTML forms are by far the most common server attack vectors
### Be paranoid: Never trust your users
* Escape potentially dangerous characters. 
* Limit the incoming amount of data to allow only what's necessary.
* Sandbox uploaded files.