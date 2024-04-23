## Preparing The Subscriber

### a. What is AMQP?

AMQP stands for Advanced Message Queuing Protocol. It's a messaging protocol that enables systems to communicate by passing messages between them. It's designed for reliability, flexibility, and interoperability. AMQP provides features like message orientation, queuing, routing (including point-to-point and publish-subscribe), reliability, and security.

### b. Explanation of URI `guest:guest@localhost:5672`

- `guest:guest`: The username and password used for authentication. In this case, both are set to `guest`.
- `localhost:5672`: Address and port of the AMQP broker.
  - `localhost`: Indicates that the broker is running on the same machine as the application.
  - `5672`: Default port for AMQP connections.
