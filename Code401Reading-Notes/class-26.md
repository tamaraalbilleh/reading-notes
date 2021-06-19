## Review, Research, and Discussion
- Name 5 Javascript UI Frameworks (other than React)
    - Ext JS by Sencha
    - Angular
    - Vue
    - Ember
    - Svelte 3

- What’s the difference between a framework and a library?
    - The key difference between a library and a framework is "Inversion of Control" : When you call a method from a library, you are in control. But with a framework, the control is inverted: the framework calls you.
    - A library can be easily replaceable by another library, but a framework cannot.
## Document the following Vocabulary Terms
- Rendering
    - Rendering is a process used in web development that turns website code into the interactive pages users see when they visit a website. The term generally refers to the use of HTML, CSS, and JavaScript codes. The process is completed by a rendering engine, the software used by a web browser to render a web page. Because of its close association with web browsers, rendering engines are commonly referred to as browser engines.
- Templates
    - a generic class or other blocks of source code that can be used as the basis for unique/personalized code units.
- State
    - The state is an instance of React Component Class can be defined as an object of a set of observable properties that control the behavior of the component it enables a component to keep track of changes between renders. 
    - the State of a component is an object that holds some information that may change over the lifetime of the component.
## Preparation Materials
### Why JSX?
* most people find it helpful as a visual aid when working with UI inside the JavaScript code. It also allows React to show more useful error and warning messages.
* Instead of artificially separating technologies by putting markup and logic in separate files, React separates concerns with loosely coupled units called “components” that contain both.
* We split JSX over multiple lines for readability. While it isn’t required, when doing this, we also recommend wrapping it in parentheses to avoid the pitfalls of automatic semicolon insertion.


* Don’t put quotes around curly braces when embedding a JavaScript expression in an attribute.
* You should either use quotes (for string values) or curly braces (for expressions), but not both in the same attribute
* Since JSX is closer to JavaScript than to HTML, React DOM uses camelCase property naming convention instead of HTML attribute names.
* If a tag is empty, you may close it immediately with />, like XML
* It is safe to embed user input in JSX

* By default, React DOM escapes any values embedded in JSX before rendering them. Thus it ensures that you can never inject anything that’s not explicitly written in your application. Everything is converted to a string before being rendered. This helps prevent XSS (cross-site-scripting) attacks.

* Babel compiles JSX down to React.createElement() calls.
### Rendering Elements
* Elements are what components are “made of”
* An element describes what you want to see on the screen
* React elements are immutable. Once you create an element, you can’t change its children or attributes. An element is like a single frame in a movie: it represents the UI at a certain point in time.
* React DOM compares the element and its children to the previous one, and only applies the DOM updates necessary to bring the DOM to the desired state.
* only the node whose contents have changed gets updated by React DOM.

