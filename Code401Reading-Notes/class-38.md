# Redux - Asynchronous Actions

- How granular should your reducers be?
    - we should use pure functions with no side-effects

- Pro or Con – multiple reducers can “fire” when a commonly named action is dispatched
    it can be a pro that you would be able to use one action to trigger multiple reducers if it is meant to be that way

- Name a strategy for preventing the above
    - name actions differently 

## Terms
- store
    - A store is an immutable object tree in Redux. A store is a state container which holds the application’s state. Redux can have only a single store in your application. Whenever a store is created in Redux, you need to specify the reducer.

- combined reducers
    - The combineReducers helper function turns an object whose values are different reducing functions into a single reducing function you can pass to createStore.
    The resulting reducer calls every child reducer, and gathers their results into a single state object.

## Preparation Materials
1. By itself, a Redux store doesn't know anything about async logic. Any asynchronicity has to happen outside the store.
2. Redux middleware were designed to enable writing logic that has side effects.
3. a Redux middleware can do anything when it sees a dispatched action: log something, modify the action, delay the action, make an async call, and more.

### [async actions](https://redux.js.org/tutorials/fundamentals/part-6-async-logic)
Redux Middleware and Side Effects#
By itself, a Redux store doesn't know anything about async logic. It only knows how to synchronously dispatch actions, update the state by calling the root reducer function, and notify the UI that something has changed. Any asynchronicity has to happen outside the store.

Earlier, we said that Redux reducers must never contain "side effects". A "side effect" is any change to state or behavior that can be seen outside of returning a value from a function. Some common kinds of side effects are things like:

- Logging a value to the console
- Saving a file
- Setting an async timer
- Making an AJAX HTTP request
- Modifying some state that exists outside of a function, or mutating arguments to a function
- Generating random numbers or unique random IDs (such as Math.random() or Date.now())

However, any real app will need to do these kinds of things somewhere. So, if we can't put side effects in reducers, where can we put them?

Redux middleware were designed to enable writing logic that has side effects.

As we said in Part 4, a Redux middleware can do anything when it sees a dispatched action: log something, modify the action, delay the action, make an async call, and more. Also, since middleware form a pipeline around the real store.dispatch function, this also means that we could actually pass something that isn't a plain action object to dispatch, as long as a middleware intercepts that value and doesn't let it reach the reducers.

Middleware also have access to dispatch and getState. That means you could write some async logic in a middleware, and still have the ability to interact with the Redux store by dispatching actions.


### [thunk middleware](https://github.com/reduxjs/redux-thunk)
A thunk is another word for a function. But it’s not just any old function. It’s a special (and uncommon) name for a function that’s returned by another. Like this:

```
function wrapper_function() {
  // this one is a "thunk" because it defers work for later:
  return function thunk() {   // it can be named, or anonymous
    console.log('do stuff now');
  };
}
```

With a plain basic Redux store, you can only do simple synchronous updates by dispatching an action. Middleware extends the store's abilities, and lets you write async logic that interacts with the store.

Thunks are the recommended middleware for basic Redux side effects logic, including complex synchronous logic that needs access to the store, and simple async logic like AJAX requests.

### [redux thunk](https://www.digitalocean.com/community/tutorials/redux-redux-thunk)
By default, Redux’s actions are dispatched synchronously, which is a problem for any non-trivial app that needs to communicate with an external API or perform side effects. Redux also allows for middleware that sits between an action being dispatched and the action reaching the reducers.

There are two very popular middleware libraries that allow for side effects and asynchronous actions: Redux Thunk and Redux Saga. In this post, you will explore Redux Thunk.

Thunk is a programming concept where a function is used to delay the evaluation/calculation of an operation.

Redux Thunk is a middleware that lets you call action creators that return a function instead of an action object. That function receives the store’s dispatch method, which is then used to dispatch regular synchronous actions inside the function’s body once the asynchronous operations have been completed.