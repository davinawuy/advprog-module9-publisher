## How much data your publisher program will send to the message broker in one run? 

Since there are 5 messeges total each having about ~29 bytes per message  there is a total size of around ~145 bytes

## The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?

They point to the same message broker meaning that they will authenticate with the same guest user and talk to the same message broker on the local machine. They will also therefore share the connection ore queue meaning that they will also communicate to the user create queue.

## Running RabbitMQ as message broker

![RabbitMQ Architecture](RabbitMQ.png)

The RabbitMQ dashboard shows thE broker is running with 1 connection, 2 queues, and 1 consumer. Message rates are currently at 0.00/s, indicating that no messages are being actively published, delivered. The spike in the graph earlier suggests that a brief burst of messages was handled. Other than that no other events are going on and the broker remains idle.

## Sending and processing event.

![Event Observing](sendandprocessevent.png)

The event I notice is that for everytime I send a message from the publisher to the subscriber side which will tnen obtain that message almost instantly. Here the machines were ran twice and therefore a total of 10 messages were sent. The messages were sent in two different groups even then this will still produce the ids from 1-5 twice.