# Templating with Mustache
## Javascript Templating
* Javascript templating is a fast and efficient technique to render client-side view templates with Javascript by using a JSON data source. 
* The template is HTML markup, with added templating tags that will either insert variables or run programming logic.
## Mustache
Mustache is a logic-less template syntax. It can be used for HTML, config files, source code — anything. It works by expanding tags in a template using values provided in a hash or object.
## Mustache-Express
Mustache Express lets you use Mustache and Express together easily
### To install:
#### **With Yarn**
`$ yarn add mustache-express`
#### **with NPM:**
`$ npm install mustache --save`
* Configure mustache-express in your server.js/app.js/index.js file:
* Create a views folder and add some html view templates (e.g. hello.html):
* Then in the router configuration, use res.render(TEMPLATE_NAME, JSON_DATA). 


# A Guide to Flexbox
## Flexbox properties
### Properties for the Parent flex container)
* display :
This defines a flex container; inline or block depending on the given value. It enables a flex context for all its direct children.
* flex-direction :
This establishes the main-axis, thus defining the direction flex items are placed in the flex container
* flex-wrap : 
By default, flex items will all try to fit onto one line. You can change that and allow the items to wrap as needed with this property.
* flex-flow :
This is a shorthand for the flex-direction and flex-wrap properties, which together define the flex container’s main and cross axes. The default value is row nowrap.
* justify-content :
![2.png](/Code301Reading-Notes/2.PNG)
* align-items
![3.png](/Code301Reading-Notes/3.PNG)
* align-content
![4.png](/Code301Reading-Notes/4.PNG)
### Properties for the Children(flex items)
* order :  controls the order in which they appear in the flex container.
* flex-grow : defines the ability for a flex item to grow if necessary. 
* flex-shrink : This defines the ability for a flex item to shrink if necessary.
* flex-basis : This defines the default size of an element before the remaining space is distributed
* flex : This is the shorthand for flex-grow, flex-shrink and flex-basis combined
* align-self : This allows the default alignment (or the one specified by align-items) to be overridden for individual flex items. 
# Flexbox Froggy
![win](https://github.com/tamaraalbilleh/reading-notes/blob/main/Code301Reading-Notes/win.PNG?raw=true)

