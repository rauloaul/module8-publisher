# Module 8 - Publisher

## Question & Answer

### a. How many data your publlsher program will send to the message broker in one run?
    
The publisher program will send 1000 data to the message broker in one run.

### b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?

The URL `guest:guest@localhost:5672` is the connection URL to the RabbitMQ server. The URL is the same in the publisher and subscriber programs because both programs are connecting to the same RabbitMQ server. The URL contains the following information:

- `guest:guest` is the username and password for the RabbitMQ server.
- `localhost:5672` is the hostname and port number of the RabbitMQ server.

## Running RabbitMQ Server
![alt text](images/image.png)