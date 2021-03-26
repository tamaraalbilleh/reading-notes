# Shay Howe’s intro to Responsive Web Design
Responsive web design is the practice of building a website suitable to work on every device and every screen size, no matter how large or small, mobile or desktop.
## Responsive vs. Adaptive vs. Mobile
* Responsive generally means to react quickly and positively to any change
* adaptive means to be easily modified for a new purpose or situation, such as change.
* responsive design websites continually and fluidly change based on different factors, such as viewport width,
* adaptive websites are built to a group of preset factors
* Mobile means to build a separate website commonly on a new domain solely for mobile users.
## Flexible Layouts
Responsive web design is broken down into three main components, including 
1. flexible layouts : the practice of building the layout of a website with a flexible grid, capable of dynamically resizing to any width.
1. media queries
1. flexible media. 

> The formula is based around taking the target width of an element and dividing it by the width of it’s parent element

`target ÷ context = result`

***
### Relative Viewport Lengths
* vw :
Viewports width
* vh :
Viewports height
* vmin :
Minimum of the viewport’s height and width
* vmax :
Maximum of the viewport’s height and width
*** 
## Flexible Grid
Taking the flexible layout concept, and formula, and reapplying it to all parts of a grid will create a completely dynamic website, scaling to every viewport size
## Media Queries
Media queries provide the ability to specify different styles for individual browser and device circumstances, the width of the viewport or device orientation
### Initializing Media Queries
There are a couple different ways to use media queries, using the @media rule inside of an existing style sheet, importing a new style sheet using the @import rule, or by linking to a separate style sheet from within the HTML document.
* Each media query may include a media type followed by one or more expressions.
* Common media types include all, screen, print, tv, and braille. and 3d-glasses
* When a media feature and value allocate to true, the styles are applied
### Logical Operators in Media Queries 
There are three different logical operators available for use within media queries, including and, not, and only.
### Media Features in Media Queries 
Media features identify what attributes or properties will be targeted within the media query expression.
### Height & Width Media Features
The height and width features are based off the height and width of the viewport rendering area, the browser window
### Orientation Media Feature
determines if a device is in the landscape or portrait orientation
### Aspect Ratio Media Features
The aspect-ratio and device-aspect-ratio features specifies the width/height pixel ratio of the targeted rendering area or output device.
### Resolution Media Feature
The resolution media feature specifies the resolution of the output device in pixel density, also known as dots per inch or DPI.
### Other Media Features
Other media features include identifying available output colors with use of the color, color-index, and monochrome features, identifying bitmap devices with the grid feature, and identifying the scanning process of a television with the scan feature. 
## Flexible Media
One quick way to make media scalable is by using the max-width property with a value of 100%. Doing so ensures that as the viewport gets smaller any media will scale down according to its containers width.
### Flexible Embedded Media
To get embedded media to be fully responsive, the embedded element needs to be absolutely positioned within a parent element. The parent element needs to have a width of 100% so that it may scale based on the width of the viewport. The parent element also needs to have a height of 0 to trigger the hasLayout mechanism within Internet Explorer.
# all about float 
## What is “Float”?
* Float is a CSS positioning property. 
* Floated elements remain a part of the flow of the web page

There are four valid  values for the float 
property:
1. Left and Right float elements those directions respectively.
2. None (the default) ensures the element will not float 
3. Inherit which will assume the float value from that elements parent element.
## What are floats used for?
* floats can be used to create entire web layouts.
* Floats are also helpful for layout in smaller instances.
## Clearing the Float
An element that has the clear property set on it will not move up adjacent to the float like the float desires, but will move itself down past the float.
Clear has four valid values as well :
1. Both is most commonly used, which clears floats coming from either direction.
2. Left and Right can be used to only clear the float from one direction respectively.
3. None is the default, which is typically unnecessary unless removing a clear value from a cascade.
4. Inherit : Clearing only the left or right float, while less commonly seen in the wild, definitely has its uses.
## The Great Collapse
If this parent element contained nothing but floated elements, the height of it would literally collapse to nothing
We fix it by clearing the float after the floated elements in the container but before the close of the container.
## Techniques for Clearing Floats
1. The Empty Div Method 
2. The Overflow Method
3. The Easy Clearing Method
## Problems with Floats
* Pushdown is a symptom of an element inside a floated item being wider than the float itself (typically an image)
* Double Margin Bug 
* The 3px Jog is when text that is up next to a floated element is mysteriously kicked away by 3px like a weird forcefield around the float
* the Bottom Margin Bug is when if a floated parent has floated children inside it, bottom margin on those children is ignored by the parent.
# Don’t Overthink It Grids
## Context
A block level element is as wide as the parent it’s inside 
## Columns
dividing the container into vertical divisions with relative or fixed widths 
# SMACSS 
## What is it?
SMACSS is a way to examine your design process and as a way to fit those rigid frameworks into a flexible thought process. It is an attempt to document a consistent approach to site development when using CSS