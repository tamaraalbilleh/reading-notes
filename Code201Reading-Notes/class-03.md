# Duckett HTML book:
## Chapter 3: Lists
### Ordered Lists
`<ol>`
`   <li>`
* ordered lists are numbered
*  Each item in the list is placed
between an opening `<li>` tag
and a closing `</li>` tag. (The li
stands for list item.)
### Unordered Lists
`<ul>`
`   <li>`
* unordered lists aren't number but have pullets 
* Each item in the list is placed
between an opening <li> tag
and a closing </li> tag. (The li
stands for list item.)
### Definition Lists
`<dl>`
`   <dt>`
`   <dd>`
* definition lists consists of a list of definitions 
* `<dt>` is used to contain the term being defiend 
*`<dd>` is used to contain the definition 
### Nested Lists
`<ul>`
`   <li>`
`      <ul>`
`         <li>`
* You can put a second list inside
an `<li>` element to create a sublist or nested list.
## Chapter 13: Boxes
### Box Dimensions : 
`width, height`
* By default a box is sized just big
enough to hold its contents
* you can use the height and
width properties with pixels,or prcentages
### Limiting Width 
`min-width, max-width`
* min-width property specifies
the smallest size a box can be
displayed at when the browser
window is narrow
* max-width property indicates
the maximum width a box can
stretch to when the browser
window is wide.
### Limiting Height
`min-height, max-height`
* same as the min amd max hieght but vertically 
* If the box is not big enough to
hold the content, and the content
expands outside the box it can
look very messy
### Overflowing Content
`overflow`
if the content contained within a box is larger than the box itself. It can have one of two values:
1. `hidden` : hides extra contetnt that does not fill the box 

1. `scroll` : adds a scroll bar to the box so the user scrolls to see missing content 
### Border, Margin & Padding
#### Border 
The border separates the edge of one box
from another 
> every box has a boarder even if it is not visible "it's value will be 0px "
#### Margin 
margins sits outside the edge of the boarder 
> when it doesn't equal zero it creates a gap boarders of two adjacent boxes
#### Padding
padding is the space between the boarder and the content inside the box 
> when it doesn't equal zero it increases the readability of its content 
### White space & Vertical Margin
* we can create spaces between items on the page by useing margins and padding 
`white space` : are the spaces between items 
### Border Width
`border-width`
* this property is used to control the thickness of a boarder 
* it can be assigned by two ways : 
1. `border-width : 3px;` useing pixles 
1. `border-width : thick;` useing values 
* we can't use precentages here
* we can assign the property for the whole borders or to a specific side like this `border-right-width : 3px;`.
### Border Style
`border-style`
* this property makes the style of the boarder different 
* it can be assigned with so many diffirent values like :
1. solid : one solid line
1. dotted : a series of square dots
1. dashed : a series of short lines
1. douple : two solid lines
1. groove :  carved into the page
1. ridge  : stick out from the page
1. inset : embedded into the page
1. outset : coming out of the page
1. hidden/none : no border
* we can assign the property for the whole borders or to a specific side like this `border-right-style : solid;`
### Border Color
`border-color`
* to assign a color to a border you can either use RGB values,hex codes or CSS color names
* we can assign the property for the whole borders or to a specific side like this `border-top-color : red;`
### Padding
`padding`
* it specify how much space there is between the box and it's content 
* we can assign the property for the whole box or to a specific side like this `padding-top : 20px ;`
### Margin
`margin`
* it specify how much space there is between the box and adjacent boxes
* we can assign the property for the whole box or to a specific side like this `margin-top : 20px ;`
### Centering Content
`margin : auto;`
* you must first sit a box width or it'll take the full page width
* left margin auto + right margin auto = box centered on the page 
### Change Inline/Block
`display`
use it either to change inline items to block level items or vice-versa, or to hide an element
`display : inline;`
block level elements --> inline elements
`display : block;`
inline elements --> block level elements
`display : inline-block;`
block level elements --> inline elements but with block level items features.
`display : none;`
This hides an element from the
page.
### Hiding Boxes
`visibility`
* The visibility property allows
you to hide boxes from users
but It leaves a space where the
element would have been.
`visibility : hidden;`
hides the element
`visibility : visible;`
shows the elemnt
### CSS3: Border Images
`border-image`
* applies an image to the border of
any box. 
* It takes a background
image and slices it into nine
pieces. 
### CSS3: Box Shadows
`box-shadow`
adds a drop shadow around the box
> needs at least the first 2 values + a color
#### Horizontal offset
puts shadow left of the box
#### Vertical offset
puts shadow top of the box
#### Blur distance
if deleted , shadow becomes solid 
#### Spread of shadow
if exsisted shadow would expand in all directions 
* if we want an inner shadow we use the word inset before these values 
### CSS3: Rounded Corners
`border-radius : value;`
* creates rounded corners 
* the value determains the size of the radius
***
# Duckett JS book:
## Chapter 2: Basic JavaScript Instructions 
### Arrays
* it is s type of variable that stores multiple values related to each other not one.
* it is useful when you don't know the exact number of values 
* to create an array we need to assign a name for it like other variables 
* values are assigned to an array inside[]
` let colors =['blue','black','red'];`
#### values in arrays 
* values inside an array are accessd as if they were a numbered list
* the list starts at zero ( not one)
> blue is number 0 , black is 1 , red is 2 
* to retrieve an item by its number 
`let itemThree; itemThree = colors[2];`
* array length holds the number of items in the array 
`let numColors = colors.length;`
### ACCESSING & CHANGING VALUES IN AN ARRAY
to access a value from an array , we put the array name followed by the number of the value 
`colors[2]= 'pink';`
## Chapter 4: Decisions and Loops 
### SWITCH STATEMENTS 
A switch statement starts with a
variable called the switch value.
Each case indicates a possible
value for this variable and the
code that should run if the
variable matches that value
#### if..else vs switch
**if..else** 
* There is no need to provide an el se
option. (You can just use an if
statement.)
* *With a series of if statements, they are
all checked even if a match has been found
(so it performs more slowly than switch). 
**SWITCH**
* You have a default option that is run if
none of the cases match.
* If a match is found, that code is run; then
the break statement stops the rest of
the switch statement running (providing
better performance than multiple i f
statements)
### TYPE COERCION & WEAK TYPING
If you use a data type JavaScript did not expect,
it tries to make sense of the operation rather
than report an error. 
### TRUTHY & FALSY VALUES
Due to type coercion, every value in JavaScript
can be treated as if it were true or false; and
this has some interesting side effects. 
* **Falsy** values are treated as if they
are fa 1 se. The table to the left
shows a hi ghScore variable with
a series of values, all of which
are falsy
* **Truthy** values are treated as if
they are true. Almost everything
that is not in the falsy table can
be treated as if it were true.
### CHECKING EQUALITY & EXISTENCE
* Because the presence of an object or array can
be considered truthy, it is often used to check
for the existence of an element within a page
* Because of type coercion, the strict equality operators ===and ! == result
in fewer unexpected values than ==and ! = do
### SHORT CIRCUIT VALUES
* Logical operators are processed left to right.
They short-circuit (stop) as soon as they have a
result - but they return the value that stopped
the processing (not necessarily true or fa 1 se). 
***
## loops
* loops check a condition. if it returns true, a code block will run .
* the condition will be checked again and it it still true, the code block will reun again.
* it repeats until the condition refurns false 
### common types of loops
1. ### for
if you want to run a code a specific number of times

* a for loop uses a counter as a condition. 
* it imstructs the code to run a specific number of times.


here you can see the condition is made up of three statments :
![IMG5](https://github.com/tamaraalbilleh/reading-notes/blob/main/Code102Reading-Notes/read007p/D5.PNG?raw=true)
* The variable is only created the first time the loop is run
* the value of i was initially set to 0
so in this case it'll run 10 times before stopping
* one is added to the counter using the incremment (++)
![img6](https://github.com/tamaraalbilleh/reading-notes/blob/main/Code102Reading-Notes/read007p/D6.PNG?raw=true)
![img7](https://github.com/tamaraalbilleh/reading-notes/blob/main/Code102Reading-Notes/read007p/d7.PNG?raw=true)

***
2. ### While 
if you don't know how many times the code should run

3. ### Do While
similer to while loop, but runs the statment inside the curly braces at least once even if the condition evaluates to false

![img4](https://github.com/tamaraalbilleh/reading-notes/blob/main/Code102Reading-Notes/read007p/D4.PNG?raw=true)

***
### KEY LOOP CONCEPTS 
* Here are three points to consider when you
are working with loops. Each is illustrated in
### USING FOR LOOPS 
A for loop is often used to loop
through the items in an array. 
### USING WHILE LOOPS
A while loop is often used to loop
through the items if you don't know how many times the code should run.
### USI NG DO WHILE LOOPS 
The key difference between
a whi 1 e loop and a do whi 1 e
loop is that the statements in
the code block come before the
condition. This means that those
statements are run once whether
or not the condition is met. 
