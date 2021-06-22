## Review, Research, and Discussion

- Can a parent component access the state of a child component?
    - Usually, the flow goes from parent to child, not the opposite
    But, there are workarounds to transfer the state from child to parent
    for example by using a library (such as Redux) that keeps the state at the application level, making it accessible from anywhere 
    - In React we can access the child’s state using Refs.  we will assign a Refs for the child component in the parent component. then using Refs we can access the child’s state.


- What can be passed along in a prop variable?
    - you can pass anything in a prop , whither it was a method or any other data type like objects , arrays ,variables etc .. 
- How can a child component “know” the state of another component?
    - ( By communicating through a shared parent )By passing a prop to other children that will trigger the parent on any change of their state, and that child will be listening to the parent state and by that it will know when a state of other children has changed.
    - Or by globalizing the state of the components like using Redux 

## Document the following Vocabulary Terms

- component props
    - Short for properties
    - Props are arguments passed into React components.
    - Props are passed to components via HTML attributes.
    - Are functions or objects that the child receive from parent. ( not sure )

- component state
    - an object that determines how that component renders & behaves.
    - an instance of React Component Class can be defined as an object of a set of observable properties that control the behavior of the component.
    - an object that holds some information that may change over the lifetime of the component.
- application state
    - Application State (also known as Program State) represents the totality of everything necessary to keep your application running. 
    - When we refer to application state we are normally referring to the state of the program as it exists in the contents of its memory.
    - This can refer to the storage that keeps the state of all the components of the app inside it

## Preparation Materials
[react basics recap](https://www.freecodecamp.org/news/these-are-the-concepts-you-should-know-in-react-js-after-you-learn-the-basics-ee1d2f4b8030/)
#### the component life cycle : it details the life of a component
![l](https://cdn-media-1.freecodecamp.org/images/1*U13Mlxz_ktcajaeJCyYkwg.png)

* A component can only be in one stage at a time

* It starts with mounting and moves onto updating > t stays updating perpetually until it gets removed from the virtual DOM. > it goes into the unmounting phase and gets removed from the DOM.

* The lifecycle methods like (componetnt did mount and component will unmount) allow us to run code at specific points in the component’s life or in response to changes in the component’s life.

### mounting :
   -  Mounting is the phase in which our React component mounts on the DOM (i.e., is created and inserted into the DOM).
    This phase comes onto the scene after the initialization phase is completed. In this phase, our component renders the first time. The methods that are available in this phase are:
        - 1. componentWillMount()
        - 2. componentDidMount()


lifecycle during mounting : 
the constructor runs > it initialize the component state > the other methods runs > the render method runs > the component mount on the dom > componentDidMount () method runs : asynchronous calls to databases or manipulate the dom directly 

### updating : 
* This phase is triggered every time state or props change.

lifecycle during updating  : 
state or props changes > getDerivedStateFromProps is called > shouldComponentUpdate runs >compares states and props and returns either true and continue rendering or false and ends the rendering > getSnapshotBeforeUpdate runs > componentDidUpdate runs : asynchronous calls to databases or manipulate the dom directly 

### unmounting : 
* When you remove a component from the DOM
* used to clean up any open connections 
lifecycle during unmounting  : 
React runs componentWillUnmount right before it gets removed.

### Other Lifecycle Methods
* forceUpdate is a method that directly causes a re-render. : it should typically be avoided.
* getDerivedStateFromError is a lifecycle method that isn’t directly part of the component lifecycle. 


### Higher-Order Components
A higher-order component is a function that takes a component and returns a new component.
* HOCs are extremely useful because they let us reuse code and remove bloat
### React State and setState()
The only way you should change state is via the setState method
* setState is asynchronous
*  setState and that is it can take a callback function. 
* setState is asynchronous, relying on it to create our new value will have some pitfalls.
### React Context
* The React context API allows you to create global context objects that can be given to any component you make. 
``` const ContextObject = React.createContext({ foo: "bar" }) ```

First, we take the initial context state, the object we passed to React.createContext() and set it as our wrapper component’s state. next we define any methods we’re going to use to change our state. Lastly, we wrap our component in the Context.Provider component. We pass in our state and function to the value prop. Now any children will get these in context when wrapped with the Context.Consumer component.



[props.children](https://codeburst.io/a-quick-intro-to-reacts-props-children-cb3d2fce4891)

* props.children on components that represent ‘generic boxes’ and that ‘don’t know their children ahead of time’.

* children does is that it is used to display whatever you include between the opening and closing tags when invoking a component.

* props.children is that it can be anything!
* help you customize your app’s content while still being able to reuse the same components. 


[composition vs inheritance](https://reactjs.org/docs/composition-vs-inheritance.html)
### Containment
 components don’t know their children ahead of time > use the special children prop to pass children elements directly into their output

 * you might need multiple “holes” in a component. (uncommon )

 * React elements like `<Contacts />` and `<Chat />` are just objects, so you can pass them as props like any other data

### Specialization
Composition works equally well for components defined as classes:

### Inheritance
Props and composition give you all the flexibility you need to customize a component’s look and behavior in an explicit and safe way






[react testing library api example](https://testing-library.com/docs/react-testing-library/example-intro/)