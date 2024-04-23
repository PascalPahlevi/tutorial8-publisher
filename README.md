# Publisher Reflection

a. How many data your publlsher program will send to the message broker in one run? <br>

In oner run, the publisher program will send 5 pieces of data to the message broker. This can be seen in the code in the main 
function as the UserCreatedEventMessage instances would create 5 messages through the use of `p.publish_event`.

b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean? <br>

The url "amqp://guest:guest@localhost:5672" is exactly the same as it is in the subscriber program, authenticating to the 
message broker with the username and password being guest. In addition to that, the publisher program is also ran
locally through the machine and is also accessible through the port 5672. This essentially creates a communication channel
between the two programs that would allow the exchange of messages to be seamless.
