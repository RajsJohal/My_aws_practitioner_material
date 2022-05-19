## Monolithic App and Micro Services
- Applications are made up of multiple components, the components communicate with each other to transmit data, fulfill requests which keep the application running. 
- An application with tightly coupled components which could be databases, servers, UI, business logic and so on, can be referred to as a monolithic application. If a single component fails so do the other components in this architecture which will then cause the entire application to fail.
- A microservice approach to the application architecture consist of loosely coupled components, if a single component fails the other components continue to work because they are still communicating with each other, thus preventing the entire application from failing.

## AWS SNS (Simple Notification Service)
- A publish/subscribe service. Using Amazon SNS topics, a publisher publishes messages to subscribers. Subscribers can be web servers, email addresses, AWS Lambda functions or several other options.

## Amazon Simple Queue Service (Amazon SQS)
- A messaging queuing service.
- You can send, store and receive messages between software components, without losing messages or requiring other ervices to be available. In Amazon SQS an application sends messages into a queue. A user or service retrieves a message from the queue, processes it and then deletes it from the queue