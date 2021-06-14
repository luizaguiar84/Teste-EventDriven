>> https://itnext.io/how-to-build-an-event-driven-asp-net-core-microservice-architecture-e0ef2976f33f
 
 The easiest way to get RabbitMQ running is to install Docker Desktop. Then issue the following command (in one line in a console window) to start a RabbitMQ container with admin UI :
 
C:\dev>docker run -d  -p 15672:15672 -p 5672:5672 --hostname my-rabbit --name some-rabbit rabbitmq:3-management


Open your browser on port 15672 and log in with the username “guest” and the password “guest”. 

Use the web UI to create an Exchange with the name “user” of type “Fanout” and two queues “user.postservice” and “user.otherservice”.

>> It is important to use the type “Fanout” so that the exchange copies the message to all connected queues.
