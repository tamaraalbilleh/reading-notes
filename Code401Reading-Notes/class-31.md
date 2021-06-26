## Review, Research, and Discussion
* Why do we not need more .html pages in a multi-page React app?
    - Because routes in React are not for exploring HTML pages, but for mounting and unmounting components

* If we wanted a component to show up on every page, where would we put it and why?
    - in the parent component 
Outside the `<BrowserRouter/>`
Inside the `<BrowserRouter />`, outside a `<Route />`
Inside a `<Route />`

    - Inside the `<BrowserRouter />`, outside a `<Route />`, because it needs to be included in the `BrowserRouter`, which holds everything, but it needs to be outside of `routes` so that they do not change or disappear no matter the chosen `Route`
    - to put the whole app inside the to wrap it inside React router, then the component that we want it to render on all pages should not be inside any meaning it does not need any specific path to render.

* What does props.children contain?
    - It is used to display whatever is passed between the parent's opening and closing tags 
## Document the following Vocabulary Terms

* Composition
    - composition is a natural pattern of the component model. It's how we build components from other components, of varying complexity and specialization through props. Depending on how generalized these components are, they can be used in building many other components.

* Children / Child Components
    - Children allow you to pass components as data to other components, just like any other prop you use. The special thing about children is that React provides support through its ReactElement API and JSX. XML children translate perfectly to React children!

* Hash Routing
    - Hash Routing A <Router> that uses the hash portion of the URL (i.e. window.location.hash) to keep your UI in sync with the URL.

* Link Routing
    - Provides declarative, accessible navigation around the application

## Preparation Materials

### [making sense of hooks](https://medium.com/@dan_abramov/making-sense-of-react-hooks-fdbde8803889)
#### Why Hooks?
We know that components and top-down data flow help us organize a large UI into small, independent, reusable pieces. However, we often can’t break complex components down any further because the logic is stateful and can’t be extracted to a function or another component. Sometimes that’s what people mean when they say React doesn’t let them “separate concerns.”
These cases are very common and include animations, form handling, connecting to external data sources, and many other things we want to do from our components. When we try to solve these use cases with components alone, we usually end up with:
Huge components that are hard to refactor and test.
Duplicated logic between different components and lifecycle methods.
Complex patterns like render props and higher-order components.

### [the state hook](https://reactjs.org/docs/hooks-state.html)
##### What is a Hook?
 A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components. We’ll learn other Hooks later.

##### When would I use a Hook?
 If you write a function component and realize you need to add some state to it, previously you had to convert it to a class. Now you can use a Hook inside the existing function component. We’re going to do that right now!

##### What do we pass to useState as an argument?
 The only argument to the useState() Hook is the initial state. Unlike with classes, the state doesn’t have to be an object. We can keep a number or a string if that’s all we need. In our example, we just want a number for how many times the user clicked, so pass 0 as initial state for our variable. (If we wanted to store two different values in state, we would call useState() twice.)

##### What does useState return?
 It returns a pair of values: the current state and a function that updates it. This is why we write const [count, setCount] = useState(). This is similar to this.state.count and this.setState in a class, except you get them in a pair. If you’re not familiar with the syntax we used, we’ll come back to it at the bottom of this page.

### [hooks api](https://reactjs.org/docs/hooks-overview.html)
The Effect Hook, useEffect, adds the ability to perform side effects from a function component. It serves the same purpose as componentDidMount, componentDidUpdate, and componentWillUnmount in React classes, but unified into a single API. (We’ll show examples comparing useEffect to these methods in Using the Effect Hook.)

##### Rules of Hooks
Hooks are JavaScript functions, but they impose two additional rules:

Only call Hooks at the top level. Don’t call Hooks inside loops, conditions, or nested functions.
Only call Hooks from React function components. Don’t call Hooks from regular JavaScript functions. (There is just one other valid place to call Hooks — your own custom Hooks. We’ll learn about them in a moment.)

### [hooks api reference](https://reactjs.org/docs/hooks-reference.html)

##### Functional updates
If the new state is computed using the previous state, you can pass a function to setState. The function will receive the previous value, and return an updated value. Here’s an example of a counter component that uses both forms of setState

##### Timing of effects
Unlike componentDidMount and componentDidUpdate, the function passed to useEffect fires after layout and paint, during a deferred event. This makes it suitable for the many common side effects, like setting up subscriptions and event handlers, because most types of work shouldn’t block the browser from updating the screen.

However, not all effects can be deferred. For example, a DOM mutation that is visible to the user must fire synchronously before the next paint so that the user does not perceive a visual inconsistency. (The distinction is conceptually similar to passive versus active event listeners.) For these types of effects, React provides one additional Hook called useLayoutEffect. It has the same signature as useEffect, and only differs in when it is fired.

Although useEffect is deferred until after the browser has painted, it’s guaranteed to fire before any new renders. React will always flush a previous render’s effects before starting a new update.

Conditionally firing an effect
The default behavior for effects is to fire the effect after every completed render. That way an effect is always recreated if one of its dependencies changes.

However, this may be overkill in some cases, like the subscription example from the previous section. We don’t need to create a new subscription on every update, only if the source prop has changed.


### [effects hook](https://reactjs.org/docs/hooks-effect.html)
##### effects Without Cleanup
Sometimes, we want to run some additional code after React has updated the DOM. Network requests, manual DOM mutations, and logging are common examples of effects that don’t require a cleanup. We say that because we can run them and immediately forget about them. Let’s compare how classes and Hooks let us express such side effects.


##### Explanation: Why Effects Run on Each Update
If you’re used to classes, you might be wondering why the effect cleanup phase happens after every re-render, and not just once during unmounting. Let’s look at a practical example to see why this design helps us create components with fewer bugs.
