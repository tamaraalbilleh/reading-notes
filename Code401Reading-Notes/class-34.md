# `<Login />` and `<Auth />`

## Review, Research, and Discussion

- Why is the Context API useful?
    - Using Context API we can define several unrelated contexts (stores) and use each in its proper place in the app.

- Can a component outside of a provider get its context?
    - probably no 

- What are some common use cases for using the Context API?
    - Theming — Pass down app theme
    - i18n — Pass down translation messages
    - Authentication — Pass down current authenticated user

- Describe “Context Hell”
    - is when multiple providers are passed as children for each other to clean up the nasty code you get from taking advantage of React Context API we need a way to nest multiple Context.Provider without passing them as children of each other. To achieve that we can use the React.cloneElement API.

## Document the following Vocabulary Terms

- global state
    - State of Component that is used by other Components and needs to be defined at the application level (app.js), to be accessible anywhere down the tree

- global context
    - Context Provider that is used for the whole App and wrap all the components.

- provider
    - The Provider component accepts a value prop to be passed to consuming components that are descendants of this Provider. One Provider can be connected to many consumers. Providers can be nested to override values deeper within the tree.

- consumer
    - A React component that subscribes to context changes. Using this component lets you subscribe to a context within a function component.

    - Requires a function as a child. The function receives the current context value and returns a React node. The value argument passed to the function will be equal to the value prop of the closest Provider for this context above in the tree. If there is no Provider for this context above, the value argument will be equal to the defaultValue that was passed to createContext().


## [what is role based access control?](https://digitalguardian.com/blog/what-role-based-access-control-rbac-examples-benefits-and-more)

### DEFINITION OF ROLE-BASED ACCESS CONTROL (RBAC)
Role-based access control (RBAC) restricts network access based on a person's role within an organization and has become one of the main methods for advanced access control. The roles in RBAC refer to the levels of access that employees have to the network.

#### Some of the designations in an RBAC tool can include:

- Management role scope – it limits what objects the role group is allowed to manage.
- Management role group – you can add and remove members.
- Management role
- these are the types of tasks that can be performed by a specific role group.
- Management role assignment – this links a role to a role group.
- By adding a user to a role group, 
- the user has access to all the roles in that group. 
- If they are removed, access becomes restricted. 
- Users may also be assigned to multiple groups in the event they need temporary access to certain data or programs and then removed once the project is complete.

#### Other options for user access may include:

- Primary – the primary contact for a specific account or role.
- Billing – access for one end-user to the billing account.
- Technical – assigned to users that perform technical tasks.
- Administrative – access for users that perform administrative tasks.

#### BENEFITS OF RBAC


- Reducing administrative work and IT support. 
- Maximizing operational efficiency.
- Improving compliance. 

#### BEST PRACTICES FOR IMPLEMENTING RBAC

- Current Status: Create a list of every software, hardware and app that has some sort of security. For most of these things, it will be a password. However, you may also want to list server rooms that are under lock and key. Physical security can be a vital part of data protection.

- Current Roles:  determining what each individual team member does may only take a little discussion. Try to organize the team in such a way that it doesn’t stifle creativity and the current culture (if enjoyed).

- Write a Policy: Any changes made need to be written for all current and future employees to see. Even with the use of a RBAC tool, a document clearly articulating your new system will help avoid potential issues.
- Make Changes: Once the current security status and roles are understood (not to mention a policy is written), it’s time to make the changes.

- Continually Adapt: It’s likely that the first iteration of RBAC will require some tweaking. Early on, you should evaluate your roles and security status frequently. 

- A core business function of any organization is protecting data. An RBAC system can ensure the company's information meets privacy and confidentiality regulations.

## [react-cookies component](https://www.npmjs.com/package/react-cookies)
Cookies are the data stored in the form of key-value pairs that are used to store information about the user on their computer by the websites that the users browse and use it to verify them.

To set or remove the cookies, we are going to use a third-party dependency of react-cookie.
## [react-cookie library](https://devdojo.com/krissanawat101/working-with-browser-cookie-in-react)
Cookies are an essential piece of component that is highly used when browsing any website in a web browser. They are small text files that store certain information about the users' device, authentication information, sessions, and other tracking information so that the user experience and interaction with the website becomes smooth and optimized.

The cookies object that we have created in our app holds all the cookies.

withCookies(Component)
Give access to your cookies anywhere. Add the following props to your component:

cookies: Cookies instance allowing you to get, set and remove cookies.
allCookies: All your current cookies in an object.
Your original static properties will be hoisted on the returned component.
