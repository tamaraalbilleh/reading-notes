# Duckett HTML book
# Ch.15 : Layout
## Key Concepts in Positioning Elements
### Building Blocks
* CSS treats each HTML element as if it is in its
own box. This box will either be a block-level
box or an inline box.
#### Block-level elements
start on a new line
Examples include:
`<h1> <p> <ul> <li`
#### flow in between
surrounding text
Examples include:
`<img> <b> <i>`
### Containing Elements
If one block-level element sits inside another
block-level element then the outer box is
known as the containing or parent element.
### Controlling the Position of Elements
CSS has the following **positioning schemes** that allow you to control
the layout of a page:
#### Normal flow
* Every block-level element
appears on a new line, causing
each item to appear lower down
the page than the previous one.
#### Relative Positioning
* This moves an element from the
position it would be in normal
flow, shifting it to the top, right,
bottom, or left of where it
would have been placed
#### Absolute positioning
This positions the element
in relation to its containing
element
### box offset properties 
* When you move
any element from
normal flow, boxes
can overlap. The
`z-index property`
allows you to control
which box appears
on top.
* To indicate where a box should be positioned

#### Fixed Positioning
This is a form of absolute
positioning that positions
the element in relation to the
browser window, as opposed
to the containing element
#### Floating Elements
Floating an element allows
you to take that element out
of normal flow and position
it to the far left or right of a
containing box. 
### Relative Positioning 
`position:relative`
Relative positioning moves an
element in relation to where it
would have been in normal flow.
### Absolute Positioning 
`position: absolute`
When the position property
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
* It positions the element in
relation to the browser window
### Overlapping Elements
`z-index`
* If you want to control which
element sits on top, you can use
the z-index property. Its value
is a number, and the higher the
number the closer that element
is to the front
### Floating Elements
`float`
* The float property allows you
to take an element in normal
flow and place it as far to the
left or right of the containing
element as possible.
### Using Float to Place Elements Side-by-Side
* When elements are floated, the
height of the boxes can affect
where the following elements sit
### Clearing Floats
`clear`
* The clear property allows you
to say that no element (within
the same containing element)
should touch the left or right-hand sides of a box. 
* It can take
the following values: left,right,both,none
### Creating Multi-Column Layouts with Floats
* Many web pages use multiple
columns in their design. This
is achieved by using a `<div>`
element to represent each
column. 
* The following three CSS
properties are used to position
the columns next to each other:width,float,margin
## Screen Sizes
* Different visitors to your site will have different sized screens that show
different amounts of information, so your design needs to be able to
work on a range of different sized screens.
## Screen Resolution
* Resolution refers to the number of dots a screen shows per inch. Some
devices have a higher resolution than desktop computers and most
operating systems allow users to adjust the resolution of their screens.
## Page Sizes
Because screen sizes and display resolutions vary so much, web
designers often try to create pages of around 960-1000 pixels wide
(since most users will be able to see designs this wide on their screens)
## Fixed Width Layouts
Fixed width layout
designs do not
change size as the
user increases
or decreases
the size of their
browser window.
Measurements tend
to be given in pixels
* To create a fixed width layout,
the width of the main boxes on
a page will usually be specified
in pixels (and sometimes their
height, too).
* The fixed width layout will stay
the same width no matter what
size the browser window is,
whereas the liquid layout will
stretch (or shrink) to fill the
screen.
## Liquid Layouts
Liquid layout designs
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
## Layout Grids
* Grids set consistent proportions
and spaces between items which
helps to create a professional
looking design. 
## CSS Frameworks
* One of the most popular uses of
CSS frameworks is in creating
grids to layout pages. 
### Multiple Style Sheets
`@import`
* Some web page authors split
up their CSS style rules into
separate style sheets
* Some authors take an even
more modular approach
to stylesheets, creating
separate stylesheets to control
typography, layout, forms,
tables, even different styles for
each sub-section of a site
* There are two ways to add
multiple style sheets to a page:
1. Your HTML page can link
to one style sheet and that
stylesheet can use the @import
rule to import other style sheets.
2. In the HTML you can use a
separate `<link>` element for
each style sheet
*** 
the end ...

