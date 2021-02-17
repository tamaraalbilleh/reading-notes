# Duckett HTML book:
## Chapter 4: Links :
### Writing Links
* Links are created using the `<a>` element. Users can click on anything
between the opening `<a>` tag and the closing `</a>` tag. You specify
which page you want to link to using the href attribute.
`<a href="http://www.imdb.com">IMDB</a>`
### Linking to Other Pages on the Same Site
* When you are linking to other
pages within the same site,
you do not need to specify the
domain name in the URL. You
can use a shorthand known as a
relative URL.
### Directory Structure
* On larger websites it's a good idea to organize your code by placing the
pages for each different section of the site into a new folder. Folders on a
website are sometimes referred to as directories.
### Relative URLs
* relative URLs can be used when linking to pages within your own
website. They provide a shorthand way of telling the browser where to
find your files.

### Email Links
* To create a link that starts up
the user's email program and
addresses an email to a specified
email address, you use the `<a>`
element. However, this time the
value of the href attribute starts
with mailto: and is followed by
the email address you want the
email to be sent to.
### Opening Links in a New Window
* One of the most common
reasons a web page author
might want a link to be opened
in a new window is if it points to
another website. In such cases,
they hope the user will return
to the window containing their
site after finishing looking at the
other one.
### Linking to a Specific Part of Another Page
* If you want to link to a specific
part of a different page (whether
on your own site or a different
website) you can use a similar
technique.
As long as the page you are
linking to has id attributes that
identify specific parts of the
page, you can simply add the
same syntax to the end of the
link for that page.

## Chapter 15: Layout
### Key Concepts in Positioning Elements
#### Building Blocks
* CSS treats each HTML element as if it is in its
own box. This box will either be a block-level
box or an inline box.
#### Containing Elements
* If one block-level element sits inside another
block-level element then the outer box is
known as the containing or parent element.
#### Controlling the Position of Elements
* CSS has the following positioning schemes that allow you to control
the layout of a page: normal flow, relative positioning, and absolute
positioning. You specify the positioning scheme using the position
property in CSS. You can also float elements using the float property.
* To indicate where a box should be positioned, you may also need to use
box offset properties to tell the browser how far from the top or bottom
and left or right it should be placed. (You will meet these when we
introduce the positioning schemes on the following pages.)
### Normal Flow
`position:static`
* in normal flow, each block-level
element sits on top of the next
one. Since this is the default
way in which browsers treat
HTML elements, you do not
need a CSS property to indicate
that elements should appear
in normal flow, but the syntax
would be:
position: static;
### Relative Positioning
`position:relative`
* Relative positioning moves an
element in relation to where it
would have been in normal flow.
### Absolute Positioning
`position:absolute`
* When the position property
is given a value of absolute,
the box is taken out of normal
flow and no longer affects the
position of other elements on
the page. (They act like it is not
there.) 
### Fixed Positioning
`position:fixed`
* Fixed positioning is a type
of absolute positioning that
requires the position property
to have a value of fixed.
### Overlapping Elements
`z-index`
* When you use relative, fixed, or
absolute positioning, boxes can
overlap. If boxes do overlap, the
elements that appear later in the
HTML code sit on top of those
that are earlier in the pag
### Floating Elements
`float`
* The float property allows you
to take an element in normal
flow and place it as far to the
left or right of the containing
element as possible.
* Anything else that sits inside
the containing element will
flow around the element that is
floated.
### Using Float to Place Elements Side-by-Side
* A lot of layouts place boxes
next to each other. The float
property is commonly used to
achieve this.
* When elements are floated, the
height of the boxes can affect
where the following elements sit
### Clearing Floats
`clear`
* The clear property allows you
to say that no element (within
the same containing element)
should touch the left or righthand sides of a box. It can take
the following values:
1. left
The left-hand side of the box
should not touch any other
elements appearing in the same
containing element.
1. right
The right-hand side of the
box will not touch elements
appearing in the same containing
element.
1. both
Neither the left nor right-hand
sides of the box will touch
elements appearing in the same
containing element.
1. none
Elements can touch either side.
### Parents of Floated Elements: Problem
* If a containing element only
contains floated elements, some
browsers will treat it as if it is
zero pixels tall.
* As you can see in this example,
the one pixel border assigned
to the containing element has
collapsed, so the box looks like a
two pixel line
### creating Multi-Column Layouts with Floats
* Many web pages use multiple
columns in their design. This
is achieved by using a `<div>`
element to represent each
column. 
* The following three CSS
properties are used to position
the columns next to each other:
1. width
This sets the width of the
columns.
1. float
This positions the columns next
to each other.
1. margin
This creates a gap between the
columns
### Screen Sizes
* Different visitors to your site will have different sized screens that show
different amounts of information, so your design needs to be able to
work on a range of different sized screens.
### Screen Resolution
* Resolution refers to the number of dots a screen shows per inch. Some
devices have a higher resolution than desktop computers and most
operating systems allow users to adjust the resolution of their screens.
### Page Sizes
* Because screen sizes and display resolutions vary so much, web
designers often try to create pages of around 960-1000 pixels wide
(since most users will be able to see designs this wide on their screens).
### Fixed Width Layouts
* Fixed width layout
designs do not
change size as the
user increases
or decreases
the size of their
browser window.
Measurements tend
to be given in pixels.
### Liquid Layouts
* Liquid layout designs
stretch and contract
as the user increases
or decreases the
size of their browser
window. They tend to
use percentages.
* The liquid layout uses
percentages to specify the width
of each box so that the design
will stretch to fit the size of the
screen.
### A Fixed Width Layout
* To create a fixed width layout,
the width of the main boxes on
a page will usually be specified
in pixels (and sometimes their
height, too)
### Layout Grids
* Composition in any visual art (such as design, painting, or photography)
is the placement or arrangement of visual elements — how they are
organized on a page. Many designers use a grid structure to help them
position items on a page, and the same is true for web designers.
### CSS Frameworks
* CSS frameworks aim to make your life easier by providing the code for
common tasks, such as creating layout grids, styling forms, creating
printer-friendly versions of pages and so on. You can include the CSS
framework code in your projects rather than writing the CSS from scratch.
### Multiple Style Sheets
`@import`
There are two ways to add
multiple style sheets to a page:
1. Your HTML page can link
to one style sheet and that
stylesheet can use the @import
rule to import other style sheets.
2. In the HTML you can use a
separate `<link>` element for
each style sheet
### Multiple Style Sheets
`link`
* On this page you can see the
other technique for including
multiple style sheets. Inside the
`<head>` element is a separate
`<link>` element for each style
sheet.
* The contents of site.css are
identical to styles.css on the
left hand page, except the code
does not contain @import rules.
* As with all style sheets, if two
rules apply to the same element
then rules that appear later in a
document will take precedence
over previous rules. 


#  Duckett JS book:
## Chapter 3 :Functions, Methods, and Objects
### WHAT IS A FUNCTION?
* Functions let you group a series of statements together to perform a
specific task. 
* **rather than repeating** the same set of statements ,If different parts of a script **repeat** the same task, you can
reuse the function
*  helps organize your code. 
* it stores the statement so they wont always be executed when the page loads .
* calling the function = naming the function a meaningful name 
* code blocks must be contained in curly braces 
* some functions need to be provided with additional info like **parameters**

### Declaring a Function
* to create a function, you give it a name and then write the statments needed to achieve it's task inside the curly braces.
* **this is called a function declaration**
![n1](https://github.com/tamaraalbilleh/reading-notes/raw/main/Code102Reading-Notes/n1.PNG)
### Calling a Function
* having ddeclared the function, you can then excute all of the statments between its curly braces with just one line of code.
* **this is called calling the function**
![n2](https://github.com/tamaraalbilleh/reading-notes/raw/main/Code102Reading-Notes/n2.PNG)
### Declaring the function that need information 
* Sometimes a function needs specific information to perform its task. In such cases, when you declare the function you give it parameters. Inside the function, the parameters act like variables. 
![n3](https://github.com/tamaraalbilleh/reading-notes/raw/main/Code102Reading-Notes/n3.PNG)
### CALLING FUNCTIONS THAT NEED INFORMATION 
* When you call a function that has parameters, you specify the values it should use in the parentheses that follow its name. The values are called arguments, and they can be provided as values or as variables. 
### declaring a function that need info
* sometimes the functions need info to wite
* you need to assign parameteres
### calling functions that need info

### getting a single value out of a function
* some functions return information to the code that called them.
for example : when they perform calculations they return the results.
### getting out a single value out of a function 
some functions return info to the code that called them for example calculation result 
### getting multiple values out of a function
some functions return more than one value using an array  to the code that called them for example 
### ANONYMOUS FUNCTIONS & FUNCTION EXPRESSIONS
* Expressions produce a value. They can be used where values are expected.
* If a function is placed where a browser expects to see an expression,
(e.g., as an argument to a function), then it gets treated as an expression.
### IMMEDIATELY INVOKED FUNCTION EXPRESSIONS

* This way of writing a function is used in several different situations.
Often functions are used to ensure that the variable names do not conflict
with each other (especially if the page uses more than one script). 

### variable scope 
* The location where you declare a variable will affect where it can be used
within your code. If you declare it within a function, it can only be used
within that function. This is known as the variable's scope. 

### HOW MEMORY & VARIABLES WORK
* Global variables use more memory. The browser has to remember them
for as long as the web page using them is loaded. Local variables are only
remembered during the period of time that a function is being executed.

# Article : 6 Reasons for Pair Programming
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