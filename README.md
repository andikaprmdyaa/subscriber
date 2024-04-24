## Preparing The Subscriber

### a. What is AMQP?

AMQP stands for Advanced Message Queuing Protocol. It's a messaging protocol that enables systems to communicate by passing messages between them. It's designed for reliability, flexibility, and interoperability. AMQP provides features like message orientation, queuing, routing (including point-to-point and publish-subscribe), reliability, and security.

### b. Explanation of URI `guest:guest@localhost:5672`

- `guest:guest`: The username and password used for authentication. In this case, both are set to `guest`.
- `localhost:5672`: Address and port of the AMQP broker.
  - `localhost`: Indicates that the broker is running on the same machine as the application.
  - `5672`: Default port for AMQP connections.

## Simulation slow subscriber

<img src="assets/images/Screenshot 2024-04-24 065143.png" alt="Rabbit Image" width="100%" height="100%">


## Reflection and Running at least three subscribers
<img src="assets/images/Screenshot 2024-04-24 070718.png" alt="Rabbit Image" width="100%" height="100%">

    When we have multiple subscribers connected to the same queue in an event-driven architecture, each subscriber competes for messages from the queue. When we spawn multiple subscribers and run them concurrently, they collectively consume messages from the queue at a faster rate compared to when we have only one subscriber. This leads to quicker processing of messages and reduces the backlog in the message queue. Additionally, when we simulate multiple requests from the publisher side by running `cargo run` several times, it increases the message flow into the queue, providing more messages for the subscribers to consume. As a result, the overall throughput of the system increases, and the backlog of messages diminishes more rapidly. This is because the workload is distributed among multiple subscribers, allowing them to process messages in parallel, leading to faster overall processing.