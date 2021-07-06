# Redux - Additional Topics
## Review, Research, and Discussion

- What’s the best practice for “pre-loading” data into the store (on application start) in a Redux application?
    - define an initial state and then use useEffect 
- When using a thunk/async action that dispatches the actual action, which do you export from your reducer?
    - the thunk action  
## Document the following Vocabulary Terms

- middleware
    - Redux middleware function provides a medium to interact with dispatched action before they reach the reducer, Each middleware receives store's dispatch so that they can dispatch new action, and getState functions as arguments so that they can access the current state and return a function
- thunk
    - Thunks are the recommended middleware for basic Redux side effects logic, including complex synchronous logic that needs access to the store, and simple async logic like AJAX requests.



## Preparation Materials

### [Redux Toolkit (RTK)](https://redux-toolkit.js.org/)


#### Getting Started with Redux Toolkit
##### Purpose#
The Redux Toolkit package is intended to be the standard way to write Redux logic. It was originally created to help address three common concerns about Redux:

- "Configuring a Redux store is too complicated"
- "I have to add a lot of packages to get Redux to do anything useful"
- "Redux requires too much boilerplate code"

We can't solve every use case, but in the spirit of create-react-app and apollo-boost, we can try to provide some tools that abstract over the setup process and handle the most common use cases, as well as include some useful utilities that will let the user simplify their application code.

Redux Toolkit also includes a powerful data fetching and caching capability that we've dubbed "RTK Query". It's included in the package as a separate set of entry points. It's optional, but can eliminate the need to hand-write data fetching logic yourself.

These tools should be beneficial to all Redux users. Whether you're a brand new Redux user setting up your first project, or an experienced user who wants to simplify an existing application, Redux Toolkit can help you make your Redux code better.


#### What's Included#
Redux Toolkit includes these APIs:

- configureStore(): wraps createStore to provide simplified configuration options and good defaults. It can automatically combine your slice reducers, adds whatever Redux middleware you supply, includes redux-thunk by default, and enables use of the Redux DevTools Extension.
- createReducer(): that lets you supply a lookup table of action types to case reducer functions, rather than writing switch statements. In addition, it automatically uses the immer library to let you write simpler immutable updates with normal mutative code, like state.todos[3].completed = true.
- createAction(): generates an action creator function for the given action type string. The function itself has toString() defined, so that it can be used in place of the type constant.
- createSlice(): accepts an object of reducer functions, a slice name, and an initial state value, and automatically generates a slice reducer with corresponding action creators and action types.
- createAsyncThunk: accepts an action type string and a function that returns a promise, and generates a thunk that dispatches pending/fulfilled/rejected action types based on that promise
- createEntityAdapter: generates a set of reusable reducers and selectors to manage normalized data in the store
- The createSelector utility from the Reselect library, re-exported for ease of use.

### [Tutorial](https://redux-toolkit.js.org/tutorials/overview)
- First of all, there is the application state. Graphs of objects, arrays, primitives, references that forms the model of your application. These values are the “data cells” of your application.
- Secondly there are derivations. Basically, any value that can be computed automatically from the state of your application. These derivations, or computed values, can range from simple values, like the number of unfinished todos, to complex stuff like a visual HTML representation of your todos. In spreadsheet terms: these are the formulas and charts of your application.
- Reactions are very similar to derivations. The main difference is these functions don't produce a value. Instead, they run automatically to perform some task. Usually this is I/O related. They make sure that the DOM is updated or that network requests are made automatically at the right time.
- Finally there are actions. Actions are all the things that alter the state. MobX will make sure that all changes to the application state caused by your actions are automatically processed by all derivations and reactions. Synchronously and glitch-free.


- Use the observable decorator or observable(object or array) functions to make objects trackable for MobX.
- The computed decorator can be used to create functions that can automatically derive value from the state and cache them.
- Use autorun to automatically run functions that depend on some observable state. This is useful for logging, making network requests, etc.
- Use the observer wrapper from the mobx-react-lite package to make your React components truly reactive. They will update automatically and efficiently. Even when used in large complex applications with large amounts of data.

## Alternative State Managers

- [MobX](https://mobx.js.org/getting-started.html)

- [HookState](https://hookstate.js.org/)
