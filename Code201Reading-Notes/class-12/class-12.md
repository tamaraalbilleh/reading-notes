# Easily Create Stunning Animated Charts With Chart.JS
## Setting up
* A great way to get started with charts is with Chart.js
* Charts.js :JavaScript plugin that uses HTML5’s canvas element to draw the graph onto the page
* charts.js makes using all kinds of bar charts, line charts, pie charts and more, incredibly easy
## Drawing a line chart
* To draw a line chart, the first thing we need to do is create a canvas element in our HTML in which Chart.js can draw our chart.
* Next, we need to write a script that will retrieve the context of the canvas
* we need to create our data, in this instance it’s an object that contains labels for the base of our chart and datasets to describe the values on the chart

## Drawing a pie chart
* First, we need the canvas element
* Next, we need to get the context and to instantiate the chart
* supply some options to the chart.
* Next we need to create the data. This data is a little different to the line chart because the pie chart is simpler, we just need to supply a value and a color for each section
## Drawing a bar chart
* the syntax for the bar chart is very similar to the line chart we’ve already added
* First, we add the canvas element
* Next, we retrieve the element and create the graph:
* And finally, we add in the bar chart’s data
***
# Chart.js

# Basic Usage
## The `<canvas>` element 
* At first sight a `<canvas>` looks like the `<img>` element
* the only clear difference being that it doesn't have the src and alt attributes
*  the `<canvas>` element has only two attributes, width and height
* When no width and height attributes are specified, the canvas will initially be 300 pixels wide and 150 pixels high

* the element can be sized arbitrarily by CSS
* The `<canvas>` element can be styled just like any normal image (margin, border, background…). These rules, however, don't affect the actual drawing on the canvas.
## fallback content
Providing fallback content is very straightforward: just insert the alternate content inside the `<canvas>` element. Browsers that don't support `<canvas>` will ignore the container and render the fallback content inside it. Browsers that do support `<canvas>` will ignore the content inside the container, and just render the canvas normally
## Required `</canvas>` tag
if `</canvas>` tag is not present, the rest of the document would be considered the fallback content and wouldn't be displayed.
## The rendering context
The canvas is initially blank. To display something, a script first needs to access the rendering context and draw on it. The `<canvas>` element has a method called `getContext()`, used to obtain the rendering context and its drawing functions. `getContext()` takes one parameter
# Drawing Shapes With Canvas
* coordinate space :canvas with the default grid overlayed. Normally 1 unit in the grid corresponds to 1 pixel on the canvas.
* `<canvas>` only supports two primitive shapes: rectangles and paths (lists of points connected by lines). All other shapes must be created by combining one or more paths. 
# Applying Styles And Colors
## Colors
* If we want to apply colors to a shape, there are two important properties we can use: `fillStyle` and `strokeStyle`.

`fillStyle = color`
Sets the style used when filling shapes.
`strokeStyle = color`
Sets the style for shapes' outlines.
* color is a string representing a CSS `<color>`, a gradient object, or a pattern object.
## Transparency
In addition to drawing opaque shapes to the canvas, we can also draw semi-transparent (or translucent) shapes. This is done by either setting the `globalAlpha` property or by assigning a semi-transparent color to the stroke and/or fill style.
* `globalAlpha = transparencyValue`
can be useful if you want to draw a lot of shapes on the canvas with similar transparency, but otherwise it's generally more useful to set the transparency on individual shapes when setting their colors.

## Line styles
There are several properties which allow us to style lines.

* `lineWidth = value`
Sets the width of lines drawn in the future.
* `lineCap = type`
Sets the appearance of the ends of lines.
* `lineJoin = type`
Sets the appearance of the "corners" where lines meet.
* `miterLimit = value`
Establishes a limit on the miter when two lines join at a sharp angle, to let you control how thick the junction becomes.
* `getLineDash()`
Returns the current line dash pattern array containing an even number of non-negative numbers.
* `setLineDash(segments)`
Sets the current line dash pattern.
* `lineDashOffset = value`
Specifies where to start a dash array on a line.
## Using line dashes
The `setLineDash` method and the `lineDashOffset` property specify the dash pattern for lines. The `setLineDash` method accepts a list of numbers that specifies distances to alternately draw a line and a gap and the `lineDashOffset` property sets an offset where to start the pattern.
## Patterns
`createPattern(image, type)`
Creates and returns a new canvas pattern object. image is a CanvasImageSource (that is, an HTMLImageElement, another canvas, a `<video> `element, or the like. type is a string indicating how to use the image.
The type specifies how to use the image in order to create the pattern, and must be one of the following string values:

`repeat`
Tiles the image in both vertical and horizontal directions.
`repeat-x`
Tiles the image horizontally but not vertically.
`repeat-y`
Tiles the image vertically but not horizontally.
`no-repeat`
Doesn't tile the image. It's used only once.
## Shadows
Using shadows involves just four properties:

`shadowOffsetX = float`
Indicates the horizontal distance the shadow should extend from the object. This value isn't affected by the transformation matrix. The default is 0.
`shadowOffsetY = float`
Indicates the vertical distance the shadow should extend from the object. This value isn't affected by the transformation matrix. The default is 0.
`shadowBlur = float`
Indicates the size of the blurring effect; this value doesn't correspond to a number of pixels and is not affected by the current transformation matrix. The default value is 0.
`shadowColor = color`
A standard CSS color value indicating the color of the shadow effect; by default, it is fully-transparent black.

# Drawing Text
The canvas rendering context provides two methods to render text:

`fillText(text, x, y [, maxWidth])`
Fills a given text at the given `(x,y)` position. Optionally with a maximum width to draw.
`strokeText(text, x, y [, maxWidth])`
Strokes a given text at the given `(x,y)` position. Optionally with a maximum width to draw.
## styling text
`font = value`
The current text style being used when drawing text. This string uses the same syntax as the CSS font property. The default font is 10px sans-serif.
`textAlign = value`
Text alignment setting. Possible values: start, end, left, right or center. The default value is start.
`textBaseline = value`
Baseline alignment setting. Possible values: top, hanging, middle, alphabetic, ideographic, bottom. The default value is alphabetic.
`direction = value`
Directionality. Possible values: ltr, rtl, inherit. The default value is inherit.
## Advanced text measurements
`measureText()`
Returns a TextMetrics object containing the width, in pixels, that the specified text will be when drawn in the current text style.
