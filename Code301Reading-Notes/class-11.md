# EJS 
> express JS
## getting started 
1. npm init -y in the terminal 
2. npm install express in the terminal 
`npm install --save express body-parser cors ejs`
3. prepare the dependencies in the server.js file "express ,cors and body parser and also path  "
4. create an instance for app to let us use the methods of express 
5. configure app using app.use 
6. using app.set to set the path of the folder we are working on 
7. set the app to listen to a port after defining a port 
8. create a rout and a handler function with a request and a response 
## injecting values into the views
in server.js :
to inject a variable we first need to define it in the response and then go to the index.ejs and add a `<%= variable name %>` in between html tags or inline of them  , `<% %>` are ejs tags .
* by writing `/<% variable %>/destroy` you delete it .
## for looping and arrays
if we had an array
```
 [ { name : 'ravi'}
    { name : 'area'}
 ]
```
and we wanted to iterate on it using for loop :
we use the for loop inside ejs tags and if we are including html markup we use the ejs tags for the content of the markup  
## if/else statements
to use an if/else statement :
```
<%= if ( if statement ){ %>
    then do this 
<% } else { %>
<% then do this  %>
<% } %>
```
we just need to enclose the statement in esj tags and write it as usual 
***
