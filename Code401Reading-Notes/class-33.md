## Review, Research, and Discussion

- Describe use cases for `useMemo()` and `useReducer()`
    - useMemo is a React hook that memorizes the output of a function. That is it. useMemo accepts two arguments: a function and a list of dependencies. useMemo will call the function and return its return value. Then, every time you call useMemo again, it will first check if any dependencies have changed. If not, it will return the cached return value, not calling the function. If they have changed, useMemo will call the provided function again and repeat the process.

    This should remind you of the useEffect hook: both useMemo and useEffect accept lists of dependencies. The only difference is that useEffect is intended for side-effects (hence the name), while functions in useMemo are supposed to be pure and with no side-effects.

    - useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one. useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.

- Why do custom hooks need the use prefix?
    - Its name should always start with use so that you can tell at a glance that the rules of Hooks apply to it. hat will indicate the usage of hooks inside it:

- What do custom hooks usually do?
    - Custom hooks allow us to have cleaner functional components, remove logic from the UI layer, and prevent code duplication by bringing common use cases to reusable hooks.

- Using any list of custom hooks, research and name one that you think will be useful in your applications
    - react-fetch-hook : useFetch hook gets us the data and the isLoading state. We can also provide the required options object to the hook.
 

- Describe how a hook that fetches API data might work
    - Fetch Data with useEffect :
    - Add a state variable using the React hook useState at the top of the function.
    - The next step is to add useEffect to the file and give the variable that stores the response data a value when the component loads.
    - API call happens when the component is mounted  , Response data is saved to the state variable
    - Import Axios at the top of the page with the line import axios from 'axios'.
    - send a request through axios to fetch data from api
    - set the response data in the variable using set-something method same as the one defined earlier  


## Document the following Vocabulary Terms

- reducer
    - A reducer is a function that determines changes to an application's state. It uses the action it receives to determine this change. We have tools, like Redux, that help manage an application's state changes in a single store so that they behave consistently.



## [context api](https://reactjs.org/docs/context.html)
### When to Use Context
Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language.

### Before You Use Context
Context is primarily used when some data needs to be accessible by many components at different nesting levels. Apply it sparingly because it makes component reuse more difficult.

This inversion of control can make your code cleaner in many cases by reducing the amount of props you need to pass through your application and giving more control to the root components. Such inversion, however, isn’t the right choice in every case; moving more complexity higher in the tree makes those higher-level components more complicated and forces the lower-level components to be more flexible than you may want.

This pattern is sufficient for many cases when you need to decouple a child from its immediate parents. You can take it even further with render props if the child needs to communicate with the parent before rendering.

However, sometimes the same data needs to be accessible by many components in the tree, and at different nesting levels. Context lets you “broadcast” such data, and changes to it, to all components below. Common examples where using context might be simpler than the alternatives include managing the current locale, theme, or a data cache.

## [hooks and context example](https://medium.com/swlh/snackbars-in-react-an-exercise-in-hooks-and-context-299b43fd2a2b)
### Dream State
From an engineering standpoint, our snackbar system must easy to use and generally be very lightweight. We want to be able to place one on the screen with just a couple of lines of code. Anything more and it’s overkill.
This means forget render props and higher order components. We don’t want to deal with a messy React tree and wrappers. We don’t want action creators, reducers*, or any of that stuff.
Hooks are a perfect fit here. So lets imagine we have a custom hook that lets us do this and work backwards.

### Globally Accessible
The state of our snackbars (which ones are visible) can be localized to a single centralized component. That same centralized component can be responsible for rendering them. There’s really no need for another component somewhere in the tree to hook into that state (at least not in our use-case).
However, the management of that state (adding, removing) needs to be globally accessible.
Context can let us do just this.

### Sprinkling in Optimizations
Our custom hook is now fully operational! We can add alerts easily from anywhere and our provider will display them for us. We could stop here, but there’s room for some optimizations that are pretty easy to achieve.
You’ll notice that value is a new object being created every single time this provider is rendered. That’s not great, because anything consuming this value from the context will potentially also be getting re-rendered.

## [react context links](https://github.com/diegohaz/awesome-react-context)

