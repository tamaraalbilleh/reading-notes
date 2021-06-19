# Readings: AWS: Events
## Review, Research, and Discussion
* Describe the similarities between AWS API Gateway + Lambda functions and an ExpressJS Server
    * in express there are routs and rout specific middleware 
* List the AWS Database offerings and talk about the pros and cons of each
    * reliable performance even as it scales;
    * a managed experience, so you won't be SSH-ing into servers to upgrade the crypto libraries;
    * a small, simple API allowing for simple key-value access as well as more advanced query patterns.is accessible via an HTTP API and performs authentication & authorization via IAM roles, making it a perfect fit for building Serverless applications.
* What’s the difference between a FIFO and a standard queue?
    * fifo doesn't have duplicate values but a standard queue can have 
* How can the server be assured a message was properly received?
    * by defining a trigger and listening to it when it gets invoked
## Document the following Vocabulary Terms
* Serverless API 
    * not needing to maintain your own servers to run these functions. it just means that the servers, the operating systems, the network layer and the rest of the infrastructure have already been taken care of, so that you can focus on writing application code.
* Triggers
    * when they happen they trigger the invocation of lambda function 
* Dynamo vs Mongo
    * Dynamo :  DynamoDB is a proprietary NoSQL database service built by Amazon and offered as part of the Amazon Web Services (AWS) portfolio , is only available on AWS.
    * Mongo : MongoDB is an open, non-tabular (enables users to update multiple rows in a table at once from a single page)database built by MongoDB, Open Source, and can be deployed anywhere.

* Dynamoose vs Mongoose
    * Dynamoose : Dynamoose is a modeling tool for Amazon's DynamoDB 
    * Mongoose L Mongoose is a MongoDB object modeling tool designed to work in an asynchronous environment
## Preparation Materials
### [AWS SQS vs SNS](https://medium.com/awesome-cloud/aws-difference-between-sqs-and-sns-61a397bf76c5)
* SQS : simple queue service : is distributed queuing service ( a message-oriented middleware or MOM deployed in a compute cloud using software as a service model. Service subscribers access queues and or topics to exchange data using point-to-point or publish and subscribe patterns.)
* SNS : simple notification  service : is a publish-subscribe service (is a pattern that allows us to create modules that can communicate with each other without depending directly on each other.)
#### SNS 
 * push notification service
 * lets you send individual messages or to bulk messages to large numbers of recipients.
 * A distributed publish-subscribe system
 * Messages are pushed to subscribers as and when they are sent by publishers to SNS
 * and then to the end points such as email, sms, http end point and SQS
 * fast, flexible, fully managed
 * simple and cost effective
 * sends to mobile device users or email recipients
 * Pull Mechanism — Consumers poll messages from SQS.
#### SQS 
* s distributed queuing system. 
* essages are not pushed to receivers. Receivers have to poll SQS to receive messages
* Messages can’t be received by multiple receivers at the same time.
* Any one receiver can receive a message, process and delete it.
* SQS is mainly used to decouple applications or integrate applications.
* Messages can be stored in SQS for short duration of time (max 14 days)
* Push Mechanism — SNS pushes messages to consumers.
<br>

[SQS and SNS Basics](https://www.youtube.com/watch?v=UesxWuZMZqI)
* You don’t have to couple SNS and SQS always
*  messaging : a massage : send between software components
* message is a json file and has key values  and attributes (value pairs)
* ques : durable ops for your message : wont be delete 
* we have two types of queues : slandered and fifo 
* using a slandered queue : you csn get duplicate values 
* using a fifo queue : you get to process the messages only once 
* you can't use  multiple approaches to deal with message queues
* every participant will recive the whole messaging queue
* message streams : an order sending of the message streams
* the difference between a queue and a stream : streams are sent as they are but when you want to open the stream you read it as if you are viewing them by like opening a cursor or an iterator on the stream and you move the iterator back and forward 
* you should use queues if you can process dependently 
* you should use streams when the order matters 
* you can take out of the stream twice a as you can put like making two titrators running on the stream 
* we can create a shard you per for it 
* the booking service should use a database
* using lambda : since it is scalable most databases wont be able to keep up
* the message is deleted from the queue only if we are done 
* queues supports long polling : process the massages using a push delivery : you make a receive call to a queue and you wait to get a message if there are any 
