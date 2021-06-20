## Review, Research, and Discussion
- Does a deployed React application require a server?
    - You don’t necessarily need a static server in order to run a Create React App project in production. It also works well when integrated into an existing server side app.

- Why do we prefer to test a React application at the behavior rather than the unit level?
    -  With components, the distinction between a “unit” and “integration” test can be blurry. If you’re testing a form, should its test also test the buttons inside of it? Or should a button component have its own test suite? Should refactoring a button ever break the form test? React is not like a function that gives a simple output, there is a visual aspect to it 
- What does npm run build do?
    - npm run build creates a build directory with a production build of your app. Set up your favorite HTTP server so that a visitor to your site is served index.html, and requests to static paths like /static/js/main.<hash>.js are served with the contents of the /static/js/main.<hash>.js file. 

    - It correctly bundles React in production mode and optimizes the build for the best performance.
    The build is minified and the filenames include the hashes.
    Behind the scenes, it uses babel to transpile your code and webpack as the build tool to bundle up your application.

- Describe the actual composition / architecture of a React application
    - React app is a set of component (component-Based) that change according to different states, and gather together to create the whole UI interface.
    - you can add functionality to a component without causing rippling changes throughout the codebase
## Document the following Vocabulary Terms
- BDD
    - Behaviour-Driven Development (BDD) is a collaborative approach to software development that bridges the communication gap between business and IT. BDD helps teams communicate requirements with more precision, discover defects early and produce software that remains maintainable over time.
    -  an Agile software development process that encourages collaboration among developers, QA, and non-technical or business participants in a software project.

- Acceptance Tests
    -Acceptance Testing is a method of software testing where a system is tested for acceptability. The major aim of this test is to evaluate the compliance of the system with the business requirements and assess whether it is acceptable for delivery or not.
    -Acceptance Testing is the last phase of software testing performed after System Testing and before making the system available for actual use.
    ![](https://media.geeksforgeeks.org/wp-content/uploads/20190429112612/Capture551.jpg)
- mounting
    -  Mounting is the phase in which our React component mounts on the DOM (i.e., is created and inserted into the DOM).
    This phase comes onto the scene after the initialization phase is completed. In this phase, our component renders the first time. The methods that are available in this phase are:
        - 1. componentWillMount()
        - 2. componentDidMount()

- build
    - creates a build directory with a production build of your app. Inside the build/static directory will be your JavaScript and CSS files. Each filename inside of build/static will contain a unique hash of the file contents

## Preparation Materials
### [setState explained](https://css-tricks.com/understanding-react-setstate/)
* React components have state.
* React components with state render UI based on that state
*  When the state of components changes, so does the component UI.
* setState() is the only legitimate way to update state after the initial state setup.
*  ***reconciliation*** : is the way React updates the DOM, by making changes to the component based on the change in state.will only update the parts of the DOM where necessary. This is why React is fast.

> Always use setState() to change state. Modifying state directly, like the snippet below will not cause the component to re-render.

* Object.assign() is used to copy data from a source object to a target object. If the data being copied from the source to the target all have same keys



> Update to a component state should be done using setState()
> You can pass an object or a function to setState()
> Pass a function when you can to update state multiple times
> Do not depend on this.state immediately after calling setState() and make use of the updater function instead.




### [handling events](https://reactjs.org/docs/handling-events.html)

* React events are named using camelCase, rather than lowercase.
* With JSX you pass a function as the event handler, rather than a string
* you cannot return false to prevent default behavior in React. You must call preventDefault explicitly.
* you don’t need to call addEventListener to a DOM element after it is created. just provide a listener when the element is initially rendered.

* if you refer to a method without () after it, such as onClick={this.handleClick}, you should bind that method. or it will return undefined


















### [forms](https://reactjs.org/docs/forms.html)
***controlled components*** : An input form element whose value is controlled by Reactو the React component that renders a form also controls what happens in that form on subsequent user input. 

* If you’ve specified a value but the input is still editable, you may have accidentally set value to undefined or null.














### [state and lifecycle](https://reactjs.org/docs/state-and-lifecycle.html)

#### Converting a Function to a Class
You can convert a function component like Clock to a class in five steps:

1. Create an ES6 class, with the same name, that extends React.Component.
2. Add a single empty method to it called render().
3. Move the body of the function into the render() method.
4. Replace props with this.props in the render() body.
5. Delete the remaining empty function declaration.

***unmounting : the DOM produced by the Class is removed.***

lifecycle methods : 

* componentDidMount :method that runs when a component mounts (method runs after the component output has been rendered to the DOM)
* componentWillUnmount : method that runs when a component unmount 
* The only place where you can assign this.state is the constructor.

***“top-down”*** or ***“unidirectional”*** data flow. Any state is always owned by some specific component, and any data or UI derived from that state can only affect components “below” them in the tree.

* You can use stateless components inside stateful components, and vice versa.









### [components and props](https://reactjs.org/docs/components-and-props.html)

* When React sees an element representing a user-defined component, it passes JSX attributes and children to this component as a single object. We call this object “props”.
* Always start component names with a capital letter.
* React treats components starting with lowercase letters as DOM tags.
* Components can refer to other components in their output. 
> if a part of your UI is used several times (Button, Panel, Avatar), or is complex enough on its own (App, FeedStory, Comment), it is a good candidate to be extracted to a separate component.

**All React components must act like pure functions with respect to their props.**
* pure : functions that do not attempt to change their inputs, and always return the same result for the same inputs.


### [React Testing Library](https://testing-library.com/docs/dom-testing-library/react-testing-library)
### [RTL Testing Example](https://thomaslombart.com/beginner-guide-testing-react-apps/)

## Bookmark
### [Roles Reference](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques#roles)

ARIA defines semantics that can be applied to elements, with these divided into roles (defining a type of user interface element) and states and properties that are supported by a role. Authors must assign an ARIA role and the appropriate states and properties to an element during its life-cycle, unless the element already has appropriate ARIA semantics (via use of an appropriate HTML element). Addition of ARIA semantics only exposes extra information to a browser's accessibility API, and does not affect a page's DOM.