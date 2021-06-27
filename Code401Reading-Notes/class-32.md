## Review, Research, and Discussion
- What does a component’s lifecycle refer to?

    - Each component in React has a lifecycle which you can monitor and manipulate during its three main phases.
    - The three phases are: Mounting, Updating, and Unmounting.

- Why do you sometimes need to “wrap” functions in useCallback when called from within useEffect
    - useCallback will help in avoiding regeneration of functions when the functional component re-renders. However there isn't much of a performance difference caused by recreation of functions.

- Why are functional components preferred over class components?
    - a functional component is written shorter and simpler, which makes it easier to develop, understand, and test. Class components can also be confusing with so many uses of this. Using functional components can easily avoid this kind of mess and keep everything clean.

- What is wrong with the following code?

```
import React, {useState, useEffect} from 'react';

function MyComponent(props) {
  const [count, setCount] = useState(0);

  function changeCount(e) {
    setCount(e.target.value);
  }

  let renderedItems = []

  for (let i = 0; i < count; i++) {
    useEffect( () => {
      console.log('component mount/update');
    }, [count]);

    renderedItems.push(<div key={i}>Item</div>);
  }

  return (<div>
     <input type='number' value={count} onChange={changeCount}/>
      {renderedItems}
    </div>);
}
```

    - using `useEffect` inside a for loop
## Document the following Vocabulary Terms

- state hook
    - A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components.

- effect hook
    - By using this Hook, you tell React that your component needs to do something after render. React will remember the function you passed (we’ll refer to it as our “effect”), and call it later after performing the DOM updates. In this effect, we set the document title, but we could also perform data fetching or call some other imperative API.

- reducer hook
    - useReducer is used to store and update states, just like the useState Hook. It accepts a reducer function as its first parameter and the initial state as the second.
    useReducer returns an array that holds the current state value and a dispatch function, to which you can pass an action and later invoke. This is similar to the pattern Redux uses but with a few differences.

## [custom hooks - all you need to know](https://www.telerik.com/kendo-react-ui/react-hooks-guide/#toc-custom-react-hooks)

Without going through all the basic Hooks again, I think we just need to revisit one of them: the useEffect Hook. I learned while reading up on Hooks on the ReactJS.org docs that there are two ways of using useEffect. You can use it without cleanup or with cleanup. These are terms I expect anyone at this stage of working with Hooks to either know or to take a few minutes to understand with the links I just provided.

With classes and before Hooks were available, side effects were placed in one of many lifecycle methods like: componentDidMount or componentDidUpdate. In cases where we have duplicated code in both of those methods (performing the same effect for mounting and updating), we can now do these things inside a functional component and we can do it with just one Hook. That's right, I'm talking about useEffect.

useEffect tells React that our component needs to do something after the component renders. It runs after the first render and after every update. In my previous articles, I only talk about side effects WITHOUT cleanup, so I would like to cover really quickly how to allow a functional component to have a side effect WITH cleanup.

## [async hooks](https://dev.to/vinodchauhan7/react-hooks-with-async-await-1n9g)
We cannot use 'async' keyword with 'useEffect' callback method. It will result in race conditions.

We are fetching our books from google api and then updating our 'setResult' state with book title. React.useEffect method will only run when our 'searchBook' got change.

## [useReducer Hook](https://reactjs.org/docs/hooks-reference.html#usereducer)
An alternative to useState. Accepts a reducer of type (state, action) => newState, and returns the current state paired with a dispatch method. (If you’re familiar with Redux, you already know how this works.)

useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one. useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.

## [react custom hooks](https://reactjs.org/docs/hooks-custom.html)
Custom Hooks offer the flexibility of sharing logic that wasn’t possible in React components before. You can write custom Hooks that cover a wide range of use cases like form handling, animation, declarative subscriptions, timers, and probably many more we haven’t considered. What’s more, you can build Hooks that are just as easy to use as React’s built-in features.

Try to resist adding abstraction too early. Now that function components can do more, it’s likely that the average function component in your codebase will become longer. This is normal — don’t feel like you have to immediately split it into Hooks. But we also encourage you to start spotting cases where a custom Hook could hide complex logic behind a simple interface, or help untangle a messy component.

## [use hooks](https://usehooks.com/)
useFirestoreQuery
Composes: useMemoCompare
This hook makes it super easy to subscribe to data in your Firestore database without having to worry about state management. Instead of calling Firestore's query.onSnapshot() method you simply pass a query to useFirestoreQuery() and you get back everything you need, including status, data, and error. Your component will re-render when data changes and your subscription will be automatically removed when the component unmounts. Our example even supports dependent queries where you can wait on needed data by passing a falsy value to the hook. Read through the recipe and comments below to see how it works.

## [hooks list](https://github.com/rehooks/awesome-react-hooks)
## [10 essential react hooks](https://blog.bitsrc.io/10-react-custom-hooks-you-should-have-in-your-toolbox-aa27d3f5564d)
* useArray hook
Array manipulation is what a dev goes through every weekday. Adding elements to an array or removing an element at a given index is a daily routine for us. useArray reduces this burden by providing us with various array manipulation methods. This hook is a part of the react-hanger package.
* react-use-form-state hook
Forms are everywhere, even in the smallest of applications we have to encounter forms and manage their state. Managing form state in React can be a bit unwieldy sometimes.
react-use-form-state is a small React Hook that attempts to simplify managing form state, using the native form input elements you are familiar with.
