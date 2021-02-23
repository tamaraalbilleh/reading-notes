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
