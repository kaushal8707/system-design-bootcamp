
 # Message-Based Communication
 
    Client Sends REQUEST in the form of Message.

    Receives RESPONSE in the form of Message.

    It is Async, so client is not required to halt the process and wait for the process.


 # Produce 

    Who is sending a REQUEST.

 # Consumer
    
    Who is receiving a REQUEST.

 # Agent

    A Channel between them producer and consumer called Agent. 

    Agent is generally a QUEUE, which follow FIFO.

    Which message will go first will receive first by a consumer.


# Message-Based Communication Model

   1. P2P Model (Peer-to-Peer Model)

    I am sending a mail to a person immediately it won't go it take some time because things will happen in a asynchronous way.

    My mail will go to the queue first and that queue follow the FIFO, after sometime my mail will go to that person to whom i sent.

    So, This is P-to-P because two Parties are getting involved. 

    Example - [ Sending a Mail ]

   2. Publish Subscribe Model 

    There are many people who has subscribed for a news letter. all person has taken a news letter subscription.

    Every morning they woke up at 6:30 am and reading News they saw there is a mail come.

    This is a Publish and Subscribed Model.

    Here Multiple Parties get Involved so only 1 Producer but multiple Consumers Involved. 

    Example - [ News letter ]


 # # Message-Based Communication Achieving Tools

    If you want to achieve in your application either P-to-P or Publish-Subscribe Model then do not write a code manually
    instead you can use Kafka or RabbitMQ. this will make your work easier.

   1. Kafka
   2. RabbitMQ