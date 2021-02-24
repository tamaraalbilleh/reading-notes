# Duckett JS book : Chapter 6: Events
## DIFFERENT EVENT TYPES 
-------------------------------------------------------
* EVENT : DESCRIPTION  

*  load  Web page has finished loading 
unload Web page is unloading (usually because a new page was requested)

 * error  Browser encounters a JavaScript error or an asset doesn't exist

* resize Browser window has been resized scroll User has scrolled up or down the page|

* EVENT DESCRIPTION
* keydown User first presses a key (repeats while key is depressed)
* keyup User releases a key
* keypress Character is being inserted (repeats while key is depressed)
 MOUSE EVENTS Occur when a user interacts with a mouse. trackpad, or touchs
* EVENT DESCRIPTION
click User presses and releases a button over the same element
dbl click User presses and releases a button twice over the same element
moused own User presses a mouse button while over an element
mouseup User releases a mouse button while over an element
mousemove User moves the mouse (not on a touchscreen)
mouseover User moves the mouse over an element (not on a touchscreen)
mouseout User moves the mouse off an element (not on a touchscreen)

## TERMINOLOGY 
### EVENTS FIRE OR ARE RAISED
When an event has occurred, it is often described as having fired or
been raised. In the diagram on the right, if the user is tapping on a link, a
### click event would fire in the browser.
EVENTS TRIGGER SCRIPTS
Events are said to trigger a function or script. When the click event
fires on the element in this diagram, it could trigger a script that enlarges
the selected item
## HOW EVENTS TRIGGER JAVASCRIPT CODE 
event handling :When the user interacts with the HTML on a web page, there are three
steps involved in getting it to trigger some JavaScript code
1. Select t he element
node(s) you want the
script to respond to. 
1. Indicate which event on
the selected node(s) will
trigger the response. 
1. State the code you want
to run when the event
occurs. 
Event handlers let you indicate which event you
### are waiting for on any particular element.
There are three types of event handlers
`. HANDLERS
See p
### HTML EVENT HANDLER ATTRIBUTES (DO NOT USE)

Please note: This approach is
now considered bad practice;
however, you need to be aware
of it because you may see it if
you are looking at older code. 
### TRADITIONAL DOM
EVENT HANDLERS
All modern browsers understand this way of creating an event handler,
but you can only attach one function to each event handler. 


## @[]E{VENT HANDLERS)
All modern browsers understand this way of creating an event handler,
but you can only attach one function to each event handler. 

### USING PARAMETERS WITH EVENT HANDLERS & LISTENERS 
Because you cannot have parentheses after the
function names in event handlers or listeners,
passing arguments requires a workaround.
Usually, when a function needs
some information to do its job,
you pass arguments within the
parentheses that follow the
function name.

### SUPPORTING OLDER VERSIONS OF IE ;
IES-8 had a different event model and did not support
addEventL i stener() but you can provide fallback code
to make event listeners work with older versions of IE. 

## EVENT GLOW
HTML elements nest inside other elemenets, if you hover or click on a link, you will also be hovering or clicking on its parent element 
## why flow matters 
the flow of events only realy matters when your code have events 
## THE EVENT OBJECT 
When an event occurs, the event object tells
you information about the event, and the
element it happened upon
## THE EVENT OBJECT IN IES-8
In IE8 and less, e will not hold
an object, so the following code
block runs and e is set to be the
event object that is a child of the
window object. 
## EVENT DELEGATION
Creating event listeners for a lot of elements
can slow down a page, but event flow allows
If users can interact with a lot of
elements on the page, such as:
1. a lot of buttons in the UI
1.  long list
1. every cell of a table
## CHANGING DEFAULT BEHAVIOR
The event object has methods that change:
the default behavior of an element and how
the element's ancestors respond to the event. 
## DIFFERENT TYPES OF EVENTS
### W3C DOM EVENTS 
The DOM events specification is
managed by the W3C (who also
look after other specifications
including HTML, CSS, and XML).
Most of the events you will meet
in this chapter are part of this
DOM events specification.
### HTM LS EVENTS 
The HTMLS specification
(that is still being developed)
details events that browsers are
expected to support that are
specifically used with HTML.
For example, events that are
fired when a form is submitted
or form elements are changed
### BOM EVENTS 
Browser manufacturers also
implement some events as part
of their Browser Object Model
(or BOM). Typically these are
events not (yet) covered by
W3C specifications (although
some will be added to W3C
specifications in the future).
Several of these events dealt
with touchscreen devices: 
`touchstart,touchend,touchmove,orientationchange`
## USER INTERFACE EVENTS
User interface CUI) events occur as a result of interaction with the
browser window rather than the HTML page contained within it,
e.g., a page having loaded or the browser window being resized
## FOCUS & BLUR EVENTS
The HTML elements you can interact with, such as links and form
elements, can gain focus. These events fire when they gain or lose focus
## MOUSE EVENTS
The mouse events are fired when the mouse is moved and also when its
buttons are clicked.
## where events occur
the event object can tell you where the cursor was positione
when an event was triggered
## KEYBOARD EVENTS
The keyboard events are fired when a user interacts with the keyboard 
## FORM EVENTS
There are two events that are commonly used with forms.
In particular you are likely to see submit used in form validation. 
## MUTATION EVENTS & OBSERVERS
Whenever elements are added to or removed from the DOM, its
structure changes. This change triggers a mutation event. 
***
 #  Duckett HTML book: Chapter 7: Forms 
## why forms ? 
The best known form on the web is probably
the search box that sits right in the middle of
Google's homepage.
## Form Controls
There are several types of form controls that
you can use to collect information from visitors
to your site.
## How Forms Work
1. A user fills in a form and then presses a button
to submit the information to the server.
2. The name of each form
control is sent to the
server along with the
value the user enters or
selects.
3. The server processes
the information using a
programming language
such as PHP, C#, VB.net,
or Java. It may also store
the information in a
database.
4. The server creates a new
page to send back to the
browser based on the
information received.
* A form may have several form controls, each
gathering different information. The server
needs to know which piece of inputted data
corresponds with which form element.
## Form Structure
### `<form>`
Form controls live inside a
`<form>` element. This element
should always carry the action
attribute and will usually have a
method and id attribute too.
### action
Every `<form>` element requires
an action attribute. Its value
is the URL for the page on the
server that will receive the
information in the form when it
is submitted.
### method
Forms can be sent using one of
two methods: get or post.
## text input 
### `<input>`
The `<input>` element is used
to create several different form
controls. The value of the type
attribute determines what kind
of input they will be creating.
### `type="text"`
When the type attribute has a
value of text, it creates a singleline text input.
### name
When users enter information
into a form, the server needs to
know which form control each
piece of data was entered into.
(For example, in a login form, the
server needs to know what has
been entered as the username
and what has been given as the
password.) Therefore, each form
control requires a name attribute.
The value of this attribute
identifies the form control and is
sent along with the information
they enter to the server.
### maxlength
You can use the maxlength
attribute to limit the number
of characters a user may enter
into the text field. Its value is the
number of characters they may
enter. For example, if you were
asking for a year, the maxlength
attribute could have a value of 4
## Password Input
### `<input>`
`type="password"`
When the type attribute has
a value of password it creates
a text box that acts just like a
single-line text input, except
the characters are blocked out.
They are hidden in this way so
that if someone is looking over
the user's shoulder, they cannot
see sensitive data such as
passwords.
### `name`
The name attribute indicates
the name of the password input,
which is sent to the server with
the password the user enters.
### `size, maxlength`
It can also carry the size and
maxlength attributes like the
the single-line text input.
## Text Area
`<textarea>`
The `<textarea>` element
is used to create a mutli-line
text input. Unlike other input
elements this is not an empty
element. It should therefore have
an opening and a closing tag. 
## `<input>`
### `type="radio"`
Radio buttons allow users to pick
just one of a number of options.
### name
The name attribute is sent to
the server with the value of the
option the user selects. When
a question provides users with
options for answers in the form
of radio buttons, the value of
the name attribute should be the
same for all of the radio buttons
used to answer that question.
### value
The value attribute indicates
the value that is sent to the
server for the selected option.
The value of each of the buttons
in a group should be different
(so that the server knows which
option the user has selected).
### checked
The checked attribute can be
used to indicate which value (if
any) should be selected when
the page loads. The value of this
attribute is checked. Only one
radio button in a group should
use this attribute.
## checkbox
### `<input>`
`type="checkbox"`
Checkboxes allow users to select
(and unselect) one or more
options in answer to a question.
### name
The name attribute is sent to
the server with the value of the
option(s) the user selects. When
a question provides users with
options for answers in the form
of checkboxes, the value of the
name attribute should be the
same for all of the buttons that
answer that question.
### value
The value attribute indicates
the value sent to the server if this
checkbox is checked.
### checked
The checked attribute indicates
that this box should be checked
when the page loads. If used, its
value should be checked.
## Drop Down List Box
### `<select>`
A drop down list box (also
known as a select box) allows
users to select one option from a
drop down list.
The `<select>` element is used
to create a drop down list box. It
contains two or more `<option>`
elements.
### name
The name attribute indicates the
name of the form control being
sent to the server, along with the
value the user selected.
### `<option>`
The `<option>` element is used
to specify the options that the
user can select from. The words
between the opening `<option>`
and closing `</option>` tags will
be shown to the user in the drop
down box.
### value
The `<option>` element uses the
value attribute to indicate the
value that is sent to the server
along with the name of the
control if this option is selected.
### selected
The selected attribute can be
used to indicate the option that
should be selected when the
page loads. The value of this
attribute should be selected.
## Multiple Select Box
`<select>`
### size
You can turn a drop down select
box into a box that shows more
than one option by adding the
size attribute. Its value should
be the number of options you
want to show at once. In the
example you can see that three
of the four options are shown.
### multiple
You can allow users to select
multiple options from this list by
adding the multiple attribute
with a value of multiple. 
## File Input Box
### `<input>`
If you want to allow users to
upload a file (for example an
image, video, mp3, or a PDF),
you will need to use a file input
box.
### type="file"
This type of input creates a
box that looks like a text input
followed by a browse button.
When the user clicks on the
browse button, a window opens
up that allows them to select a
file from their computer to be
uploaded to the website.
## submit button 
`<input>`
### type="submit"
The submit button is used to
send a form to the server.
### name
It can use a name attribute but it
does not need to have one.
### value
The value attribute is used to
control the text that appears
on a button. It is a good idea to
specify the words you want to
appear on a button because the
default value of buttons on some
browsers is ‘Submit query’ and
this might not be appropriate for
all kinds of form.
## Image Button
`<input>`
### type="image"
If you want to use an image for
the submit button, you can give
the type attribute a value of
image. The src, width, height,
and alt attributes work just
like they do when used with the
`<img>` element
## Button & hidden Controls
### `<button>`
The `<button>` element was
introduced to allow users more
control over how their buttons
appear, and to allow other
elements to appear inside the
button.
### `<input>`
type="hidden"
This example also shows a
hidden form control. These form
controls are not shown on the
page (although you can see them
if you use the View Source option
in the browser). They allow web
page authors to add values to
forms that users cannot see.
## Grouping Form Elements
### `<fieldset>`
You can group related form
controls together inside the
`<fieldset>` element. This is
particularly helpful for longer
forms.
### `<legend>`
The `<legend>` element can
come directly after the opening
`<fieldset>` tag and contains a
caption which helps identify the
purpose of that group of form
controls.
## search input 
### `<input>`
If you want to create a single
line text box for search queries,
HTML5 provides a special type
of input for that purpose.
### type="search"
If you want to create a single
line text box for search queries,
HTML5 provides a special
search input
# Duckett HTML book: Chapter 14: Lists, Tables & Forms (pp.330-357)
## bullet point styles
`list-style-type`
* The list-style-type property
allows you to control the shape
or style of a bullet point (also
known as a marker).
It can be used on rules that
apply to the `<ol>`, `<ul>`, and `<li>`
elements.
## Images for Bullets 
`list-style-image`
* The value starts with the letters
url and is followed by a pair
of parentheses. Inside the
parentheses, the path to the
image is given inside double
quotes.
## positioning the marker
`list-style-position`
* Lists are indented into the page
by default and the list-style-position property indicates
whether the marker should
appear on the inside or the
outside of the box containing the
main points. 
## List Shorthand
`list-style`
As with several of the other CSS
properties, there is a property
that acts as a shorthand for list
styles. It is called list-style,
and it allows you to express
the markers' style, image and
position properties in any order.
## table properties 
1. `width` to set the width of the
table
2. `padding` to set the space
between the border of each table
cell and its content
3. `text-transform` to convert the
content of the table headers to
uppercase
4. `letter-spacing`, font-size
to add additional styling to the
content of the table headers
5. `border-top, border-bottom`
to set borders above and below
the table headers
6. `text-align` to align the writing
to the left of some table cells and
to the right of the others
7. `background-color` to change
the background color of the
alternating table rows
8. `:hover` to highlight a table row
when a user's mouse goes over it
## border on empty cells 
`empty-cells`
Since browsers treat empty cells
in different ways, if you want to
explicitly show or hide borders
on any empty cells then you
should use this property.
## Gaps Between Cells
`border-spacing, border-collapse`
The border-spacing property
allows you to control the
distance between adjacent cells.
By default, browsers often leave
a small gap between each table
cell, so if you want to increase
or decrease this space then
the border-spacing property
allows you to control the gap.
## Styling Fieldsets & Legends
* Fieldsets are particularly helpful
in determining the edges of a
form. In a long form they can
help group together related
information within it.
* The legend is used to indicate
what information is required in
the fieldset.
## Aligning Form Controls: Problem
Labels for form elements are
often different lengths, which
means that the form controls will
not appear in a straight line. This
is demonstrated in the example
on the right (without CSS applied
to the form controls
## cursor styles
`cursor`
The cursor property allows
you to control the type of mouse
cursor that should be displayed
to users
***
 the end ..


