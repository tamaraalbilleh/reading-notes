## Review, Research, and Discussion
* Write the following steps in the correct order:
    1. Register your application to get a client_id and client_secret
    2. Ask the client if they want to sign in via a third party
    3. Redirect to a third party authentication endpoint
    4. Make a request to the third-party API endpoint
    5. Receive authorization code
    6. Make a request to the access token endpoint
    7. Receive access tokent
* What can you do with an authorization code?
    *  make a request to get an access token
* What can you do with an access token?
    * The access token represents the authorization of a specific application to access specific parts of a user's data. Access tokens must be kept confidential in transit and in storage.
* What’s a benefit of using OAuth instead of your own basic authentication?
    * It allows limited access to the user's data and allows accessing when authorization tokens expire. It has ability to share data for users without having to release personal information. It is easier to implement and provides stronger authentication
## Document the following Vocabulary Terms

* Client ID
    * The Client ID (cid) is a unique identifier for a browser–device pair that helps Google Analytics link user actions on a site. By default, Google Analytics determines unique users using this parameter.
* Client Secret
    Client Secret  is a secret used by the OAuth Client to Authenticate to the Authorization Server,a  secret known only to the OAuth Client and the Authorization Server.
* Authentication Endpoint
    * Endpoint authentication is an authentication mechanism used to verify the identity of a network's external or remote connecting device. These endpoint devices include laptops, smartphones, tablets, and servers. This method ensures that only valid or authorized endpoint devices are connected to a network.
* Access Token Endpoint
    * The token endpoint is where apps make a request to get an access token for a user. This section describes how to verify token requests and how to return the appropriate response and errors. Authorization Code
* API Endpoint
    *  is one end of a communication channel. When an API interacts with another system, the touchpoints of this communication are considered endpoints.
* Authorization Code
    * An authorization code is an alphanumeric password that authorizes its user to purchase, sell or transfer items, or to enter information into a security-protected space.
* Access Token
    * An access token is a tiny piece of code that contains a large amount of data. Information about the user, permissions, groups, and timeframes is embedded within one token that passes from a server to a user's device.

## Preparation Materials
### Introduction to JSON Web Tokens
### If you can decode JWT, how are they secure?
