# Data Modeling
## Review, Research, and Discussion
* Name 3 advantages to Test Driven Development
    * Writing the tests first requires 
    * you to really consider what do 
    * you want from the code.
    * You receive fast feedback.
    * TDD creates a detailed specification.
* In what case would you need to use beforeEach() or afterEach() in a test suite?
    * `beforeEach()` removes the explicit calls from the tests themselves
    * `afterEach()` invites inexperienced users to share state between tests.
* What is one downside of Test Driven Development
    * the tests need to be maintained because the code has got to. Whenever requirements change you need to change the code and test . 
* What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?
    * class defines a type which can be instantiated at runtime and has constructor that generates an object, whereas a prototype is itself an object instance.
* Why REST?
    * REST is Easy to Understand and Implement
    * REST principles can help increase your dev team's productivity.
    * Many people know about REST and HTTP so it will be much easier for them to understand and use your API.
    *  REST Makes your Application More Scalable because of :
        * No State : only keep resources (memory) occupied when they are handling a request and they free it as soon as the request is processed.
        * Faster Data Interchange Format :use JSON as the data interchange format. JSON is much more compact and smaller in size compared to XML.
    * Caching is Easier with REST : Since the server is stateless and each request can be processed individually
    
***
## Document the following Vocabulary Terms
* functional programming 
    * is the process of building software by composing pure functions, avoiding shared state, mutable data, and side-effects. Functional programming is declarative rather than imperative, and application state flows through pure functions. Contrast with object oriented programming, where application state is usually shared and colocate with methods in objects.
* object-oriented programming (OOP) 
    * Object Oriented programming (OOP) is a programming paradigm that relies on the concept of classes and objects. It is used to structure a software program into simple, reusable pieces of code blueprints (usually called classes), which are used to create individual instances of objects.
* class
    * class Templates for creating objects. The constructor() method is used for creating and initializing an object created with a class.
* super
    * The super keyword refers to the parent class. It is used to call the constructor of the parent class and to access the parent’s properties and methods.
* this
    * this refers to the current object himself if inside an object 
    * this refers to the window object if global 
* Test Driven Development (TDD)
    * is a software development process relying on software requirements being converted to test cases before software is fully developed, and tracking all software development by repeatedly testing the software against all test cases. This is opposed to software being developed first and test cases created later. 
* Jest
    * is a JavaScript testing framework maintained by Facebook, Inc. designed and built by Christoph Nakazawa with a focus on simplicity and support for large web applications. 
* Continuous Integration (CI)
    Continuous integration (CI) is the practice of automating the integration of code changes from multiple contributors into a single software project.
* REST
    * REST Representational state transfer (REST) is a software architectural style which uses a subset of HTTP. It is commonly used to create interactive applications that use Web services. A Web service that follows these guidelines is called RESTful
* Data Model
    * A data model provides the details of information to be stored, and is of primary use when the final product is the generation of computer software code for an application or the preparation of a functional specification to aid a computer software make-or-buy decision.
***
## noSQL vs SQL
### SQL vs NoSQL: High-Level Differences
| SQL | nonSQL |
|-----|------|
| primarily called as Relational Databases (RDBMS) | primarily called as non-relational or distributed database. |
| table based databases | document based databases |
| have predefined schema | have dynamic schema|
| vertically scalable | horizontally scalable |
|scaled by increasing the horse-power of the hardware | scaled by increasing the databases servers in the pool of resources|
| uses SQL ( structured query language ) for defining and manipulating  | queries are focused on collection of documents The syntax of using UnQL varies from database to database|
|MySql, Oracle, Sqlite, Postgres and MS-SQL|MongoDB, BigTable, Redis, RavenDb, Cassandra, Hbase, Neo4j and CouchDb|
|good fit for the complex query intensive environment | not good fit for complex queries.|
|not best fit for hierarchical data storage|fits better for the hierarchical data storage|
|vertically scalable.|horizontally scalable|
|best fit for heavy duty transactional type applications|not comparable and sable enough in high load and for complex transactional applications.|
|Excellent support are available for all SQL database from their vendors.|some NoSQL database you still have to rely on community support, and only limited outside experts are available for you to setup and deploy your large scale NoSQL deployments|
| emphasizes on ACID properties ( Atomicity, Consistency, Isolation and Durability)| follows the Brewers CAP theorem ( Consistency, Availability and Partition tolerance )|
| either open-source or close-sourced from commercial vendors| can be classified on the basis of way of storing data as graph databases, key-value store databases, document store databases, column store database and XML databases|

*** 
[NOSQL DATA MODELING TECHNIQUES](https://highlyscalable.wordpress.com/2012/03/01/nosql-data-modeling-techniques/)


