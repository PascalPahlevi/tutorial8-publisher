# Publisher Reflection

a. How many data your publlsher program will send to the message broker in one run? <br>

In oner run, the publisher program will send 5 pieces of data to the message broker. This can be seen in the code in the main 
function as the UserCreatedEventMessage instances would create 5 messages through the use of `p.publish_event`.

b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean? <br>

The url "amqp://guest:guest@localhost:5672" is exactly the same as it is in the subscriber program, authenticating to the 
message broker with the username and password being guest. In addition to that, the publisher program is also ran
locally through the machine and is also accessible through the port 5672. This essentially creates a communication channel
between the two programs that would allow the exchange of messages to be seamless.

-----------------------------------------------------------------------------------------------------------------------------------------------
# RabbitMQ Screenshot
<img width="1280" alt="image" src="https://github.com/PascalPahlevi/tutorial8-publisher/assets/143638456/bb7b6b88-a0fb-46b5-a303-9cb062d902ff">

-----------------------------------------------------------------------------------------------------------------------------------------------
# Console Screenshot
<img width="1280" alt="image" src="https://github.com/PascalPahlevi/tutorial8-publisher/assets/143638456/4a86be08-e58d-48cc-899c-99ef5e089c07">
While running the both subscriber and publisher, they both connect to one another through the usage of amqp://guest:guest@localhost:5672. The messages received on subscriber was sent by the publisher through the AMQP message
broker. Essentially, the subcriber program listens for the `user_created` instances then proceeds to print out these messages, in this case totalling 5. On the other hand, the publisher program creates and sends out multiple `user_created`
instance for the subscriber program to listen to.
