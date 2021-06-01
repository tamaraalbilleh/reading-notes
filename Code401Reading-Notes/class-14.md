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
    * A FIFO queue is a queue that operates on a first-in, first-out (FIFO) principle. This means that the request (like a customer in a store or a print job sent to a printer) is processed in the order in which it arrives.
* Pub/Sub
    * Pub/Sub is an asynchronous messaging service that decouples services that produce events from services that process events.
    * You can use Pub/Sub as messaging-oriented middleware or event ingestion and delivery for streaming analytics pipelines.

***
## [AWS SNS and SQS](https://www.youtube.com/watch?v=mXk0MNjlO7A)
| SNS | SQS |
|-----|-----|
| simple notification service | simple queue service |
| Pub/Sub system | queueing service for message processing |
| publisher sends to subscribers a message | messages have to be polled to discover new events  , messages are processed by a single consumer |
| if other systems care about the events | if your system care about the event |

Amazon Simple Queue Service (SQS) and Amazon SNS are both messaging services within AWS, which provide different benefits for developers. Amazon SNS allows applications to send time-critical messages to multiple subscribers through a “push” mechanism, eliminating the need to periodically check or “poll” for updates. Amazon SQS is a message queue service used by distributed applications to exchange messages through a polling model, and can be used to decouple sending and receiving components. Amazon SQS provides flexibility for distributed components of applications to send and receive messages without requiring each component to be concurrently available.

