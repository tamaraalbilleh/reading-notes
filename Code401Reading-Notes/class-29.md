## Review, Research, and Discussion
- Do child components have direct access to props/state from the parent?

    - Yes, children can access parent's state and props from parent
    - we can add a method that handles updating the state to the parent component and pass the method as a prop to the child component instead of the state itself
    - to do so :
        - In Parent Component create a method that accepts some data and sets the accepted data as the parent's state.
        - Pass the method created in Parent to child as props.
        - Accept the props in parent using this.props followed by method name and pass child's state to it as argument.
        - The method will replace the parent's state with the child's state.


- When a component “wraps” another component, how does the child component’s output get rendered?
    - It gets rendered inside the props.children in the parent component
    - You can set an if statement with condition as an prop for the parent component, and when that condition is met you can use props.children which will render all children inside of it.


- Can a component, such as <Content />, which is a child also be used as a standalone component elsewhere in the application?
    ```
    <Main>
        <Content />
    </Main>
    ```
    - yes it can be a stand alone component and be rendered any where else in the app as long as it's content do not depend on the parent content.

- What trick can a parent use to share all props with it’s children
    super(props),props.children --> all the children content or other component wrapped between the opening and closing parent element,composition --> is the process of wrapping parent with children component (component composition) and then control the appearance of the children by the parent.

## Document the following Vocabulary Terms

- props.children
    - The code or tags between open and close parent tag.
    - property allows you to create a generic template component that can be modified by the parent when it is invoked. This means that a parent component can pass whatever is needed in the child component, even generated layout features that can then be rendered by the child.

- composition
    - React Composition is a development pattern based on React's original component model where we build components from other components using explicit defined props or the implicit children prop.
    - Creating a unique component from a generic/reusable component


## Preparation Materials

[browser router tutorial](https://blog.pshrmn.com/simple-react-router-v4-tutorial/)
#### Installation
React Router has been broken into three packages: react-router, react-router-dom, and react-router-native.

You should almost never have to install react-router directly. That package provides the core routing components and functions for React Router applications. The other two provide environment specific (browser and React Native) components, but they both also re-export all of react-router's exports.

We are building a website (something that will be run in browsers), so we will install react-router-dom.

`npm install --save react-router-dom`
#### The Router
When starting a new project, you need to determine which type of router to use. For browser based projects, there are `<BrowserRouter>` and `<HashRouter>` components. The `<BrowserRouter>` should be used when you have a server that will handle dynamic requests (knows how to respond to any possible URI), while the `<HashRouter>` should be used for static websites (where the server can only respond to requests for files that it knows about).

Usually it is preferable to use a `<BrowserRouter>`, but if your website will be hosted on a server that only serves static files, then the `<HashRouter>` is a good solution.

For our project, we will assume that the website will be backed by a dynamic server, so our router component of choice is the `<BrowserRouter>`.

#### History
Each router creates a history object, which it uses to keep track of the current location 1 and re-render the website whenever that changes. The other components provided by React Router rely on having that history object available through React’s context, so they must be rendered as descendants of a router component. A React Router component that does not have a router as one of its ancestors will fail to work.

If you are interested in learning more about the history object (I think that this is important), you can check out my blog post A Little Bit of History.

[browser router api docs](https://reactrouter.com/web/api)
#### useLocation
The useLocation hook returns the location object that represents the current URL. You can think about it like a useState that returns a new location whenever the URL changes.This could be really useful e.g. in a situation where you would like to trigger a new “page view” event using your web analytics tool whenever a new page loads
#### useParams
useParams returns an object of key/value pairs of URL parameters. Use it to access match.params of the current `<Route>`.
#### useRouteMatch
The useRouteMatch hook attempts to match the current URL in the same way that a `<Route>` would. It’s mostly useful for getting access to the match data without actually rendering a `<Route>`.
#### `<BrowserRouter>`
A `<Router>` that uses the HTML5 history API (pushState, replaceState and the popstate event) to keep your UI in sync with the URL.

##### basename: string
The base URL for all locations. If your app is served from a sub-directory on your server, you’ll want to set this to the sub-directory. A properly formatted basename should have a leading slash, but no trailing slash.
##### getUserConfirmation: func
A function to use to confirm navigation. Defaults to using window.confirm.
##### null matches
A `<Route>` that uses the children prop will call its children function even when the route’s path does not match the current location. When this is the case, the match will be null. Being able to render a `<Route>`'s contents when it does match can be useful, but certain challenges arise from this situation.The default way to “resolve” URLs is to join the match.url string to the “relative” path.
If you attempt to do this when the match is null, you will end up with a TypeError. This means that it is considered unsafe to attempt to join “relative” paths inside of a `<Route>` when using the children prop.A similar, but more subtle situation occurs when you use a pathless `<Route>` inside of a `<Route>` that generates a null match object.
##### matchPath
This lets you use the same matching code that `<Route>` uses except outside of the normal render cycle, like gathering up data dependencies before rendering on the server.
#### wrappedComponentRef: func
A function that will be passed as the ref prop to the wrapped component.