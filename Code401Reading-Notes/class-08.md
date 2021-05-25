## Review, Research, and Discussion
* When is Basic Authorization used vs. Bearer Authorization?
    * Basic Auth authenticate using username and secret. it sends username and secret as plain text.
    * Bearer Auth" authenticate using access_token.

* What does the JSON Web Token package do?
    * JSON Web Token JWT is an open standard that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed
* What considerations should we make when creating and storing a SECRET?
    * Never store un encrypted secrets in .git repositories. Avoid git add * commands on git. Add sensitive files in .gitignore. 
    * Don’t rely on code reviews to discover secrets.
    * Don’t share your secrets un encrypted in messaging systems like slack.
    * Store secrets safely.
    * Restrict API access and permissions.

## Document the following Vocabulary Terms
* encryption   
    * is the method by which information is converted into secret code that hides the information's true meaning. The science of encrypting and decrypting information is called cryptography.
* token
    * When the system has authenticated the user, instead of repeating this process for every request, a token is created that represents the fact that the user is authenticated. This token is then used in subsequent requests. In this case the something is the fact the the user is authenticated, and the token represents this fact.
* bearer
    * Bearer authentication (also called token authentication) is an HTTP authentication scheme that involves security tokens called bearer tokens.
    * The client must send this token in the Authorization header when making requests to protected resources:
* secret
    * Client Secret is a secret used by the OAuth Client to Authenticate to the Authorization Server.
    * The Client Secret is a secret known only to the OAuth Client and the Authorization Server.
    * Client Secret must be sufficiently random to not be guessable.
* JSON Web Token
    * JSON Web Token is a standard used to create access tokens for an application. It works this way: the server generates a token that certifies the user identity, and sends it to the client

## Role Based Access Control (RBAC)
* in enterprise setting : access may be based on job function or role of a user 

### benefits 
* policies don't need to be updated when a certain person with a role leaves the organization .
* new comers should be able to activate the desired role  
* Revisiting least privilege by limiting access to certain files , so if they missed up they wont affect the remaining files
* SELinux supports RBAC 
## 5 steps to simple role-based access control (RBAC)
the idea of assigning system access to users based on their role within an organization. The system needs of a given workforce are analyzed, with users grouped into roles based on common job responsibilities and system access needs
### Benefits of RBAC?
* it can in reality be easy to implement, and will make the ongoing management of access rights much easier and more secure.
* prevents data breach
### RBAC vs. ABAC 
* Access control lists (ACL) — An ACL is a means of defining access rights by a given user or user group, to a specific object, such as a document. 
* Attribute-based access control (ABAC) — ABAC, sometimes known as policy-based access control, can use a variety of attributes, including user department, time of day, location of access, type of access required, etc. to determine whether a user’s access request should be granted.
###  RBAC implementation 
1. Inventory your systems
    * Figure out what resources you have for which you need to control access, if you don't already have them listed.
2. Analyze your workforce and create roles
    * group your workforce members into roles with common access needs.  Avoid the temptation to have too many roles defined. 
3. Assign people to roles
    * figure out which role(s) each employee belongs in, and set their access accordingly. 
4. Never make one-off changes
    * Resist any temptation to make a one-off change for an employee with unusual needs.
5. Audit
    * Periodically review your roles, the employees assigned to them, and the access permitted for each.






