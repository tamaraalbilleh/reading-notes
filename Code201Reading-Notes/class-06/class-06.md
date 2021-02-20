# Duckett JS book
## Chapter 3: Object Literals
## WHAT IS AN OBJECT? 
* objects group together a set of variables and functions to create a model of a something you would recognize from the real world , but in different names .
* variables in objects become property and it tells us about the object
* functions in objects become methods and it is the tasks that are associated with the object
* keys are the names of properties like the ones that variables have , and also the names of methods like the ones functions have .
* there can't be two objects with the same key (name).
* properties can take other objects as values 
* methods can only contain functions 
## creating an object :
* literal notation is the easiest way to create objects 
* the object is stored in a variable and is the curly braces and their content .
![objects](/class-06/object1.PNG)
## accessing an object and dot notation
* using dot notation helps accessing methods and properties within an object 
* we use the name of the object followed by a period (member operator which means the thing on the right is a member of the one on the left ) then the name of the property or method we want to access .
![objects](/class-06/object2.PNG)

## Chapter 5: Document Object Model
### THE DOM TREE IS A MODEL OF A WEB PAGE 
* As a browser loads a web page, it creates a model of that page.
The model is called a DOM tree, and it is stored in the browsers' memory.
It consists of four main types of nodes.
* Each node is an object with methods and properties.
Scripts access and update this DOM tree (not the source HTML file).
Any changes made to the DOM tree are reflected in the browser. 
![nodes](/class-06/nodes1.PNG)
####  THE DOCUMENT NODE 
* At the top of the tree a document node is added it represents the entire page
*  It is
the starting point for all visits to the DOM tree.
####  ELEMENT NODES 
* HTML elements describe the structure of an HTML page (like tags )

####  ATTRIBUTE NODES 
* Attribute nodes are not children of the element thar
carries them; they are part of that element
####  TEXT NODES 
* Once you have accessed an element node, you
can then reach the text within that element. This is
stored in its own text node. 
* text nods can't have children
### WORKING WITH THE DOM TREE
Accessing and updating the DOM tree involves two steps: 
1. Locate the node that represents the element you want to work with. 
1. Use its text content, child elements, and attributes. 


## step one : ACCESS THE ELEMENTS
#### DOM queries to select individual elements
1. `getElementByld ()`
Uses the value of an element's
id attribute (which should be
unique within the page).
2. `querySelector ()`
Uses a CSS selector, and returns
the first matching element.
#### DOM queries to select multiple elements
1. `getElementsByClassName()`
Selects all elements that have
a specific value for their cl ass
attribute. 
2. `getElementsByTagName()`
Selects all elements that have the
specified tag name .
3.` querySelectorAll()` 
Uses a CSS selector to select all
matching elements. 
####  traversing the DOM
You can move from one element
node to a related element node. 
1. `parentNode`
Selects the parent of the current
element node (which will return
just one element). 
2. `previousSibling` / `nextSibling`
Selects the previous or next
sibling from the DOM tree. 
3. `firstChild` / `lastChild`
Select the first or last child of the
current element.
## step two : WORK W ITH THOSE ELEMENTS
### ACCESS/ UPDATE TEXT NODES
1. `nodeValue`
This property lets you access or
update contents of a text node.
2. `textContent`
This property lets you access or
update contents of a text node.
3. `innerHTML`
This property lets you access to
child elements **and** text content:
#### DOM manipulation
`create Element()` 
`createTextNode()`
`appendChild ()` / `removeChild ()`
### ACCESS OR UPDATE ATTRIBUTE VALUES
Here are some of the properties
and methods you can use to
work with attributes:
1. `className` /`id`
Lets you get or update the value
of the class and id attributes.
`hasAttribute()` checks if an attribute
exists.
`getAttribute()`  gets its value.

`setAttribute()`   updates the value.

`removeAttribute()` removes an attribute.
### caching DOM queries
* queries are methods that find elements in the DOM
* if we want to work with an element more then once we should use a variable to store the result of the query.
* caching the selections :  when storing elements in a variable we are actually storing the location of the element within thr dom tree (like storing a reference to the element)
### ACCESSING ELEMENTS
* DOM queries may return one element, or they may return a Nodelist,
which is a collection of nodes. 
#### GROUPS OF ELEMENT NODES 
* Nodelist : a collection of
nodes.
* You then need to select the element you want from
this list using an index number (which means the
* numbering starts at 0 like the items in an array). 

#### FASTEST ROUTE 
* Finding the quickest way to access an element
within your web page will make the page seem
faster and/or more responsive.
##### METHODS THAT RETURN A SINGLE ELEMENT NODE: 
`getElementByld ('id')`
`querySelector( 'css selector')`
search an entire document and return individual elements
##### METHODS THAT RETURN ONE OR MORE ELEMENTS (AS A NODELIST): 
* Nodelists look like arrays and are numbered like
arrays, but they are not actually arrays; they are a
type of object called a **collection**.
`getElementsByClassName( 'class ')` 
`getEl ementsByTagName( 'tagName')`
`querySelectorAll ('css selector')`
* In a live Nodelist, when your script updates the
page, the Nodelist is updated at the same time. 
* In a static Nodelist when your script updates the
page, the NodeList is not updated to reflect the
changes made by the script. 
### SELECTING AN ELEMENT FROM A NODELIST
There are two ways to select an element from a Nodelist:
1. The item() method   
2. array syntax [].(better)
* Both require the index number of the element you want.
### repeating actions for entire nodlist 
* If you want to apply the same
code to numerous elements,
looping through a Nodelist is a
powerful technique.
JAVASCRIPT
* It involves finding out how many
items are in the Nodelist, and
then setting a counter to loop
through them, one-by-one.
* Each time the loop runs, the
script checks that the counter
is less than the total number of
items in the Nodelist. 
### whitespace nodes 
Traversing the DOM can be difficult because
some browsers add a text node whenever they
come across whitespace between elements. 
### HOW TO GET/UPDATE ELEMENT CONTENT 
To work with the content of elements you can:
*  Navigate to the text nodes. This works best
when the element contains only text, no other
elements.
*  Work with the containing element. This allows
you to access its text nodes and child elements.
It works better when an element has text nodes
and child elements that are siblings
#### CONTAINING ELEMENT
When you are working with an element node (rather
than its text node), that element can contain markup.
You have to choose whether you want to retrieve
(get) or update (set) the markup as well as t he text.
1. innerHTML : Gets/sets text & markup 
2. textContent : Gets/sets text only
3. innerText : Gets/sets text only 
### ACCESS & UPDATE A TEXTNODE WITH NODEVALUE
When you select a text node, you can retrieve or amend the content of it using the `nodeValue` property which returns
the text in that text node or updates the content
of a text node
### ACCESS & UPDATE TEXT WITH TEXTCONTENT (& INNERTEXT)
The textContent property allows you to
collect or update just the text that is in the
containing element (and its children). 
1. `textContent` To collect the text from elements(and ignore any markup inside
the element)
2. `innerText`  you should generally avoid it for three key reasons: 1. support : firefox does not support it , 2. obeys css : if content is hidden by css it will not show them 3. performance : it is slower to retrieve .
### ACCESS & UPDATE TEXT & MARKUP WITH INNERHTML
* When getting HTML from an
element, the innerHTML property
will get the content of an
element and return it as one long
string, including any markup that
the element contains
* When used to set new content
for an element, it will take a
string that can contain markup
and process that string, adding
any elements within it to the
DOM tree. 
* When adding new content using
innerHTML, be aware that one
missing closing tag could throw
out the design of the entire page. 
### ADDING ELEMENTS USING DOM MANIPULATION
1. `createElement ()`
 This element node is stored in a variable. 
2. `createTextNode()` 
creates a new text node. Again, the node is stored in a variable.
3. `appendChild()` adds node to DOM tree 
### REMOVING ELEMENTS VIA DOM MANIPULATION
1. STORE THE ELEMENT TO BE REMOVED IN A VARIABLE

2. STORE THE PARENT OF THAT ELEMENT IN A VARIABLE

3. REMOVE THE ELEMENT FROM ITS CONTAINING ELEMENT:`removeChild() `
### COMPARING TECHNIQUES: UPDATING HTML CONTENT
* `document.write()`
The document object's write () method is a simple
way to add content that was not in the original
source code to the page, but its use is rarely advised. 
* `element.innerHTML`
The innerHTML property lets you get/update the
entire content of any element (including markup) as
a string. 
* DOM MANIPULATION
: refers to using a set of methods
and properties to access, create, and update
elements and text nodes. 
### CROSS-SITE SCRIPTING (XSS) ATTACKS
* XSS involves an attacker placing malicious code into
a site
* XSS can give the attacker access to information in:
• The DOM (including form data)
• That website's cookies
• Session tokens: information that identifies you
from other users when you log into a site
### DEFENDING AGAINST CROSS-SITE SCRIPTING
#### VALIDATE INPUT GOING TO THE SERVER 
* Only let visitors input the kind
of characters they need to when
supplying information.
* Double-check validation on
the server before displaying user
content/storing it in a database.
* The database may safely
contain markup and script
from trusted sources (e.g., your
content management system).
*  Do not create DOM fragments
containing HTML from untrusted
sources. 
* Make sure that you are only
inserting content generated by
users into certain parts of the
template files 
* As your data leaves the
database, all potentially
dangerous characters should be
escaped 
* Make sure that your users can only input characters they need to use and limit where this content will be shown on the page.
* Any content generated by users that contain characters that are used
in code should be escaped on the server. 
### attribute nodes
you can use other properties and methods on element nodes to access and change its attributes 
![attribute nodes](/class-06/nodes2.PNG)
### CHECK FOR AN ATTRIBUTE AND GET ITS VALUES
The `hasAttribute()` method
of any element node lets you
check if an attribute exists.
 The
attribute name is given as an
argument in the parentheses.
### CREATING ATTRIBUTES & CHANGING THEIR VALUES
The `setAttribute()` method
allows you to update the value
of any attribute. It takes two
parameters: the attribute name,
and the value for the attribute
### REMOVING ATTRIBUTES
the  `removeAttribute ()` It has one parameter: the name
of the attribute to remove. 
***
## Understanding the problem domain is the hardest part of programming
* hardest thing about writing code learning the problem domain.
* Many of the problem domains we face as programmers are difficult to understand and look completely different depending on your viewpoint
* Programming is easy if you understand the problem domain
* You can often make the problem domain easier by cutting out cases and narrowing your focus to a particular part of the problem.
* It is easy to fall into the trap of thinking you understand enough of the problem to get started coding it
