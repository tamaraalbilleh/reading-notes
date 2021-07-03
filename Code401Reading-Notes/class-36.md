# Application State with Redux


* What are the advantages of storing tokens in “Cookies” vs “Local Storage”
1. local storage : 
Pros: It's convenient. If you don't have a back-end and you're relying on a third-party API, 
Cons: It's vulnerable to XSS attacks.
2. Cookies
Pros: The cookie is not accessible via JavaScript; hence, it is not as vulnerable to XSS attacks as localStorage.If you're using httpOnly and secure cookies, that means your cookies cannot be accessed using JavaScript. 
Cons: you might not be able to store your tokens in the cookies. Cookies have a size limit of 4KB. Therefore, if you're using a big JWT Token, storing in the cookie is not an option.

* Explain 3rd party cookies.


Third-party cookies are cookies that are set by a website other than the one you are currently on. For example, you can have a "Like" button on your website which will store a cookie on a visitor's computer, that cookie can later be accessed by Facebook to identify visitors and see which websites they visited. Such a cookie is considered to be a 3rd party cookie.

* How do pixel tags work?

A snippet of code is added to your website to create a 1×1 pixel graphic. The tiny size makes it unlikely to be noticed by visitors, and tracking pixels are usually designed to blend in with your existing site or be transparent. When a user visits your site, the tracking pixel loads to collect information about them as they browse your website.

A tracking pixel can gather a lot of information about users and how they interact with your site. Some data points that 
- can be collected include:

    - Which pages they view
    - Which ads they click on
    - The operating system they use
    - The type of device they use
    - The screen resolution they use
    - What time they visited
    - Activities during a session
    - Their IP addresses

## Document the following Vocabulary Terms

* cookies
    * Cookies are the data stored in the form of key-value pairs that are used to store information about the user on their computer by the websites that the users browse and use it to verify them. To set or remove the cookies, we are going to use a third-party dependency of react-cookie.

* authorization
    * Authorization is the function of specifying access rights/privileges to resources, which is related to general information security and computer security, and to access control in particular. More formally, "to authorize" is to define an access policy

* access control
    * Access control is a security technique that regulates who or what can view or use resources in a computing environment. It is a fundamental concept in security that minimizes risk to the business or organization.

* conditional rendering
    * Conditional rendering is a term to describe the ability to render different user interface (UI) markup if a condition is true or false. In React, it allows us to render different elements or components based on a condition


## Preparation Materials
### [Dan Abramov Redux Tutorials](https://egghead.io/courses/fundamentals-of-redux-course-from-dan-abramov-bd5cc867)
1. the whole state of your application is represented as a single js object is called the state or the state-tree

2. state tree is redundant , any time you want to change the tree you need to dispatch an action (js object describing the change in the application in a minimal way) minimum requirement : requires a type property which can not be undefined that would describe what the action is about
    - any data that gets into a redux application gets there by actions.

3. pure functions : function that their return values depends solely on the values of their arguments and if we call the same functions with the same set of arguments we will get the same result while impure functions may have side effects or call a database or overwrite a value that is passed to them

4. UI is most predictable when it is described as a pure function of the application state , the state mutations need to be described as a pure function  that takes the previous state and the action and returns the next state (has to be pure to return a new object and not mutate the old one)
    - the reducer : to describe state mutations you have to create a pure function that takes the prev state of the app and the action being dispatched and returns the next state of the app 

5. the reducer function accepts state and action and returns new state based on actions type , and the initial state if the type is unrecognizable or if the state is undefined . 

> cdn : A CDN (Content Delivery Network) is a highly-distributed platform of servers that helps minimize delays in loading web page content by reducing the physical distance between the server and the user. This helps users around the world view the same high-quality content without slow loading times

6. store.getState () : retrieves the current state of the redux store 
    - store.dispatch ({type : 'something'})  : dispatches actions to let you change the state of your application 
    - store.subscribe (callback function usually render) : is called anytime an action has been dispatched and updates the ui ,  it subscribes to the changes and calls the callback function on those changes 

7. store can be implemented from scratch if we have a reducer function created 

8. deep-freeze : makes sure the app is free of mutations , you can't push or mutate an array in the state
    - use concat or spread operator rather then push
    - use slice rather then splice then concat
    - use slice and concat rather than redefining an array item 
    - use object.assign the new value and return it or spread operator rather then ! that mutates the state 
   
### [worlds easiest guide to redux](https://www.freecodecamp.org/news/understanding-redux-the-worlds-easiest-guide-to-beginning-redux-c695f45546f6/)
Redux is a pattern and library for managing and updating application state, using events called “actions”.

It helps you write applications that behave consistently, run in different environments (client, server, and native), and are easy to test. On top of that, it provides a great developer experience.

Redux helps you manage “global” state - state that is needed across many parts of your application.

## Benefits
Technical benefits of using Redux.
Predictable states. The state is always predictable in Redux.
Ease in maintenance. 
Debugging is easy. 
Testing code is simple.
Server rendering. 
Vast developer tools available. 
Great supportive community. 
Reusable Code.

## Purpose
Redux is a predictable state container designed to help you write JavaScript apps that behave consistently across client, server, and native environments and are easy to test. While it's mostly used as a state management tool with React, you can use it with any other JavaScript framework or library.

### [testing reducers](https://medium.com/@netxm/testing-redux-reducers-with-jest-6653abbfe3e1)

#### Reducers
Just a quick refresher on what reducer is before we go into testing and code. Redux documentation is still great, in fact it covers unit tests really well you don’t even have to read this post. To summarize it, the reducer is a pure function that takes the previous state and an action, and returns the next state.

#### Pure functions
Because it’s a pure function, it’s easy to test. It’s a function that produces no side effects; given the same input, will always return the same output; doesn’t rely on external state.

#### What to test
Usually reducer consists of initial state and switch statement to handle every action. I like to break down my store into different sub-stores and have separate reducers for each sub-store. Sometimes one switch/case may handle few actions, because the business logic is the same and outcome should be the same. Some example GET_POST and UPDATE_POST should update the same store and produce same outcome.
It’s important to test reducers. That’s where business logic should happen and where new application state is formed based on external (API) or internal response.

#### Boilerplate
As any unit test, it starts with boilerplate setup and writing empty tests just to outline what needs to be tested. I like to to test the initial state and then every switch/case in the reducer to see if action.payload will produce expected store. If you stop and think about it — it’s simple.
### [Redux Docs](https://redux.js.org/)

#### Redux Store
Ultimately, the "store" is where your application state is, well, stored. The store's job is to identify the various reducers and middleware that need to be made available and used globally.

React uses "reducers" to hold and manage state. Reducers typically manage just one part of the larger application state. For example, in a storefront application, you would likely have a separate reducer for Products, Categories, and Carts