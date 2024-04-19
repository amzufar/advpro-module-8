# Tutorial 8
Pada tutorial ini, saya belajar mengenai Event Driven Programming menggunakan Rust. Sumber: [medium/geekculture](https://medium.com/geekculture/event-driven-programming-with-rust-and-rabbitmq-using-crosstown-bus-c39c50ce6c98)
## Refleksi
a. What is **amqp**?

AMQP (Advanced Message Queuing Protocol) is used to set up a communcation channel between different parts of a software system. Specifically, it is used for message passing between components or services. The code on `main.rs` initializes a message queue listener using the `CrosstownBus` library, which implements the AMQP protocol. This listener connects to a message broker (later on we will be using RabbitMQ) located at the URL `"amqp://guest:guest@localhost:5672"`. So AMQP is being used in this code to facilitate communication between different parts of a distributed system by passing messages between them through a message broker.

b. What it means? guest:guest@localhost:5672, what is the first **guest**, and what is the second **guest**, and what is **localhost:5672** for?

`guest:guest` represents the username and password used to authenticate with the AMQP server. In this case, both the username and password are set to `"guest"`. `localhost:5672` represents the hostname IP address and port number of the AMQP server. `localhost` referes to the local machine. Meaning the AMQP server is expected to be running on the same computer where the code is executed. `5672` refers to be the default port number for AMQP communication.
