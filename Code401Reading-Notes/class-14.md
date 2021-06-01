## Review, Research, and Discussion
* What’s the difference between a FIFO and a standard queue?
    * Standard queues provide best-effort ordering which ensures that messages are generally delivered in the same order as they are sent. Occasionally (because of the highly-distributed architecture that allows high throughput), more than one copy of a message might be delivered out of order.
    * FIFO queues offer first-in-first-out delivery and exactly-once processing: the order in which messages are sent and received is strictly preserved.
* How can the server be assured a message was properly received?
    * include a nonce (one time password or id) with each sent message.
    * The client sends a confirmation message that they received successfully.
* What classic design pattern is best represented by event driven programming?
    * Behavioral (Observer) design pattern
* How do you test an event driven system?
    * by testing the events through firing events with static data.


## Document the following Vocabulary Terms
* FIFO Queue
* Pub/Sub

***
[AWS SNS and SQS](https://www.youtube.com/watch?v=mXk0MNjlO7A)
