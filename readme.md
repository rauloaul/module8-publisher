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

## Sending and processing event
![alt text](images/image2.png)

### Explanation :
- At first, I run `cargo run` on subscriber's directory, and the subscriber program will wait for the data from the message broker.

- After that, when I run `cargo run` on publisher's directory, the publisher program will send 5 data to the message broker. 

- Then, the subscriber program will receive the data from the message broker and process the data.

## Monitoring chart based on publisher
![alt text](images/image3.png)

### Explanation :

The spike on the "message rates" chart is caused by the publisher program sending data to the message broker. The spike occurs when the publisher program sends data to the message broker. The spike represents the number of messages sent by the publisher program to the message broker.

clarification : I accidentally uncommented `// thread::sleep(ten_millis);` on the first run, so I had to revised the screenshot (yes, The initial commit main.rs on subscriber had the sleep uncommented)