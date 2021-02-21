# Duckett HTML book: Chapter 6 : Tables
## What's a Table?
* A table represents information in a grid format. 
* Each block in the grid is referred
to as a table cell. 
* In HTML a table is written out row by row.
## Basic Table Structure
### `<table>`
The `<table>` element is used
to create a table. The contents
of the table are written out row
by row.
### `<tr>`
You indicate the start of each
row using the opening `<tr>` tag.
(The tr stands for table row.)
### `<td>`
Each cell of a table is
represented using a `<td>`
element. (The td stands for
table data.)
## table heading
### `<th>`
The `<th>` element is used just
like the `<td>` element but its
purpose is to represent the
heading for either a column or
a row. (The th stands for table
heading.)
* Even if a cell has no content,
you should still use a `<td>` or
`<th>` element to represent
the presence of an empty cell
otherwise the table will not
render correctly
## Spanning ColumnS
* Sometimes you may need the
entries in a table to stretch
across more than one column.
The `colspan attribute` can be
used on a `<th>` or `<td>` element
and indicates how many columns
that cell should run across.
## Spanning rows
* You may also need entries in
a table to stretch down across
more than one row.
The `rowspan attribute` can be
used on a `<th>` or `<td>` element
to indicate how many rows a cell
should span down the table.
## Long Tables
There are three elements that
help distinguish between the
main content of the table and
the first and last row
### `<thead>`
The headings of the table should
sit inside the `<thead>` element.
### `<tbody>`
The body should sit inside the
`<tbody>` element.
### `<tfoot>`
The footer belongs inside the
`<tfoot>` element
## Old Code
### Width & Spacing
* The width attribute was used
on the opening `<table`> tag to
indicate how wide that table
should be and on some opening
`<th>` and `<td>` tags to specify
the width of individual cells.
The value of this attribute is
the width of the table or cell in
pixels
### Border & Background
* The `border attribute` was used
on both the` <table>` and `<td>`
elements to indicate the width of
the border in pixels.
* The `bgcolor attribute` was used
to indicate background colors
of either the entire table or
individual table cells. The value
is usually a hex cod

# Duckett JS Book: Chapter 3 : Functions, Methods, and Objects
## creating an object : constructor notation 
* using the object () constructor function 
` let objectName = new object ();{    statements ; other statements }; `
## updating an object 
* to delete property we use delete keyword `delete objectName.propertyName`
* to clear the property of an object we use `objectName.propertyName='';`
* to update the value of properties we use dot notations `objectName.propertyName= 'new value';`
* or we use the square brackets `objectName['propertyName'] ='new value';`
## CREATING MANY OBJECTS: CONSTRUCTOR NOTATION
* if we want to create several objects , we can use a function as a template for creating object, like creating a function with a certain use 
and then creating separate object each invoking the same functions but with different sets of parameters
## THIS (IT IS A KEYWORD)
* The keyword this is commonly used inside functions and objects
* It always refers
to one object, usually the object in which the function operates.
* global scope or global context: When a function is created at the top level of a script
(that is, not inside another object or function)
* when this is used inside a function in the
global context it refers to the window object
## A METHOD OF AN OBJECT
* When a function is defined inside an object, it
becomes a method. 
* In a method, this refers to the
containing object.
## RECAP: STORING DATA
### VARIABLES
* A variable has just one key (the variable name) and one value.
### ARRAY
* Arrays can store multiple pieces of information.
Each piece of information is separated by a comma.
The order of the values is important because items
in an array are assigned a number (called an index)
* If you want to access items via a property name or key, use an object 
*  each key in the object must be unique
* If the order of the items is important, use an array. 
### INDIVIDUAL OBJECTS 
* Objects store sets of name/value pairs. They can be
properties (variables) or methods (functions).
* Objects created with literal notation are good:
1. W hen you are storing I transmitting data
between applications
2. For global or configuration objects that set up
information for the page
###  MULTIPLE OBJECTS
When you need to create multiple objects within the
same page, you should use an object constructor to
provide a template for the objects. 
* Objects created with constructors are good when:
1. You have lots of objects used with similar
functionality (e.g., multiple slideshows I media
players/ game characters) within a page
2. A complex object might not be used in code
## arrays are objects
arrays are a special type of object 
> but the key for each value is its index
## arrays of objects and objects in arrays 
* you can create complex data structure by combining arrays and objects 
### arrays in objects 
* the property of an object can hold an array
### objects in arrays 
* the value of any element in an array can be an object
## WHAT ARE BUILT-IN OBJECTS?
Browsers come with a set of built-in objects that represent things like the
browser window and the current web page shown in that window.
### WHAT IS AN OBJECT MODEL? 
An object model is a group of objects, each of
which represent related things from the real world.
Together they form a model of something larger
1. BROWSER OBJECT MODEL:
The Browser Object Model contains
objects that represent the current
browser window or tab. It contains
objects that model things like
browser history and the
device's screen
![1](./1.png)
2. DOCUMENT OBJECT MODEL
The Document Object Model uses
objects to create a representation of
the current page. It creates a new
object for each element (and each
individual section of text)
within the page. 
> It represents the web page loaded into the current browser window or tab.
![2](./2.png)
![3](./3.png)
3. GLOBAL JAVASCRIPT OBJECTS
The global JavaScript objects
represent things that the JavaScript
language needs to create a model
of. For example, there is an
object that deals only with
dates and times.
![4](./4.png)
## DATA TYPES REVISITED
In JavaScript there are six data types: 
1. String
2. Number
3. Boolean
4. Null :a variable with no value
5. Undefined :no value has been assigned to it yet
6. object : arrays and functions are considered
types of objects
## GLOBAL OBJECTS: NUMBER OBJECT
Whenever you have a value that is a number,
you can use the methods and properties of the
Number object on it.
![5](./5.png)
## MATH OBJECT TO CREATE RANDOM NUMBERS 
![6](./6.png)
## creating an instance of the date object 
to work with dates we create date objects.
* to create date objects :
`let today = new Date ()`
## GLOBAL OBJECTS: DATE OBJECT (AND TIME)
Once you have created a Date object, the following methods let you set
and retrieve the time and date that it represents
![7](./7.png)

# Domain Modeling
* Domain modeling is the process of creating a conceptual model in code for a specific problem
* object-oriented model :  An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an object-oriented model.
* To define the same properties between many objects, you'll want to use a constructor function
* the constructor function is defined using a function expression
* When modeling a single entity that'll have many instances, build self-contained objects with the same attributes and behaviors.
* Model its attributes with a constructor function that defines and initializes properties.
* Model its behaviors with small methods that focus on doing one job well.
* Create instances using the new keyword followed by a call to a constructor function.
* Store the newly created object in a variable so you can access its properties and methods from outside.
* Use the this variable within methods so you can access the object's properties and methods from inside.