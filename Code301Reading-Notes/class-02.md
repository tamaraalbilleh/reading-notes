# JQUERY
## what is Jquery ?
is a javaScript file that you include in your web pages that lets you find elements using CSS selectors , and do something with them using Jquery methods .
* the methods represents tasks that is needed to perform with the elements yoy found 
## WHY USE JQUERY? 
it allows you to achieve 
the same goals but in fewer lines of code than you would need to write 
with plain JavaScript.
1. SIMPLE SELECTORS 
1. COMMON TASKS IN LESS CODE 
1. CROSS-BROWSER COMPATIBILITY
## a matched set / Jquery selection
when you select one or more elements , a jquery object is returned as a matched set or a jquery selection.
* single element => the object contains a reference to a one element node
* multiple elements => the object contains a reference to each element 
## Jquery methods that gets and sets data 
they receive from or update the information of the content of the elements they are applied on .
* `.html(update)` => to update content
* `.html()` => to get content
## caching Jquery selections in variable 
to create a jquery object :
1. find the matching node in the DOM tree
1. create the jquery object 
1. store reference to the nodes in the jquery object .
## LOOPING 
* With jQuery, when a selector 
returns multiple elements, you 
can update all of them using the 
one method. There is no need to 
use a loop. 
* The ability to update all of the 
elements in the jQuery selection 
is known as implicit iteration. 
## CHAINING 
The process of placing several 
methods in the same selector is 
referred to as chaining
* `hide()` hides the elements 
* `delay ()` creates a pause 
* `fade In ()` fades in the elements 
 ## GETTING ELEMENT CONTENT
 The • htm 1 () and • text () methods both retrieve and update the content 
of elements.
## UPDATING ELEMENTS 
* `html()` 
This method gives every element 
in the matched set the same new 
content. The new content may 
include HTML. 
* `.replaceWith() `
This method replaces every 
element in a matched set with 
new content. It also returns the 
replaced elements. 
* `. text() `
This method gives every element 
in the matched set the same new 
text content. Any markup would 
be shown as text. 
* `. remove() `
This method removes all of the 
elements in the matched set.
## INSERTING ELEMENTS 
Inserting new elements involves two steps: 
1. Create the new elements in a jQuery object 
2. Use a method to insert the content into the page 
## GETTING AND SETTING 
ATTRIBUTE VALUES 
You can create attributes, or access and update their contents
`.attr() ,. removeAttr() ,. addCl ass() ,.removeClass() `
## GETTING & SETTING CSS PROPERTIES 
The `. css ()` method lets you retrieve 
and set the values of CSS properties. 
## WORKING WITH EACH ELEMENT IN A SELECTION
Query allows you to recreate the functionality of a loop on a selection of elements, using the `. each ()` method. 
* `• each() `Allows you to perform one or 
more statements on each of 
the items in the selection of 
elements that is returned by a 
selector - rather like a loop in 
JavaScript.
* `this` or `$(this)` 
As the . each() method goes 
through the elements in a 
selection, you can access the 
current element using the this 
keyword.
## EVENT METHODS 
The` • on ()` method is used to handle all events
Using the `. on ()` method is no 
different than using any other 
jQuery method; you: 
* Use a selector to create a 
jQuery selection. 
* Use `. on()` to indicate which 
event you want to respond to. 
It adds an event listener to 
each element in the selection. 
## THE EVENT OBJECT 
Every event handling function receives an event object. 
It has methods and properties related to the event that occurred. 
![i](/Code301Reading-Notes/1.PNG)
## ADDITIONAL PARAMETERS FOR EVENT HANDLERS 
The `• on ()` method has **two**  optional properties that let you: 
Filter the initial jQuery selection to respond to a subset of the elements; 
Pass extra information into the event handler using object literal notation. 
## ways to include Jquery in your page 

hosting the jquery file with the rest of the website , in addition to that you can use a version that is hosted by another company but you still need to include the fallback version 
## LOADING JQUERY FROM A CDN
a protocol 
relative URL :used When a page loads jQuery from 
a CDN
`<script src=" //ajax .googl eapi s . com/ ajax/l i bs/ jquery / 1.10. 2/ jquery .min. js "></ script>`
## WHERE TO PLACE YOUR SCRIPTS 
* The position of `<script>` elements can affect 
how quickly a web page seems to load. 
* if you place the script at the end of the 
page before the closing `</body>` tag, it will not affect 
the rendering of the rest of the page. 
*** 
# 6 Reasons for Pair Programming
6 Reasons for Pair Programming
> “two heads are better than one”
pair programming is the practice of two developers sharing a single workstation to interactively tackle a coding task together
## How does pair programming work?
pair programming commonly involves two roles:
1. The Driver is the programmer who is typing and the only one whose hands are on the keyboard
> manages the text editor, switching files, version control, and—of course writing—code
1. The Navigator uses their words to guide the Driver but does not provide any direct input to the computer
## Why pair program?
there are four fundamental skills that help anyone learn a new language: 
1. Listening: hearing and interpreting the vocabulary 
1. Speaking: using the correct words to communicate an idea 
1. Reading: understanding what written language intends to convey 
1. Writing: producing from scratch a meaningful
Pair programming touches on all four skills
* and it gives : 
1. Greater efficiency : it is easier to catch mistakes in the making+  may come to a solutions faster
1. Engaged collaboration : knowing when to ask for help
1. Learning from fellow students :If one programmer is more experienced in a certain skill, they can teach a student who is less familiar with that area
1. Social skills : communication is key.
1. Job interview readiness: the ability to work with and learn from others and stellar communication skills are as (or more!) important to a company than specific technical skills
1. Work environment readiness : graduates who are already familiar with how pairing works can hit the ground running at a new job, with one less hurdle to overcome