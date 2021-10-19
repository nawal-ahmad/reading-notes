# Read: 19 - Spring and Sockets

## Using WebSocket to build an interactive web application

what is a web socket?
- **WebSocket** is a thin, lightweight layer above TCP. This makes it suitable for using “subprotocols” to embed messages.
- **STOMP** is a subprotocol operating on top of the lower-level WebSocket.

### steps:

- Create a Resource Representation Class:
The service will accept messages that contain a name in a STOMP message whose body is a JSON object.

- Create a Message-handling Controller
create a controller to receive  and send the messages.
 STOMP messages can be routed to @Controller classes like the following:

 ```
 package com.example.messagingstompwebsocket;

import org.springframework.messaging.handler.annotation.MessageMapping;
import org.springframework.messaging.handler.annotation.SendTo;
import org.springframework.stereotype.Controller;
import org.springframework.web.util.HtmlUtils;

@Controller
public class GreetingController {


  @MessageMapping("/hello")
  @SendTo("/topic/greetings")
  public Greeting greeting(HelloMessage message) throws Exception {
    Thread.sleep(1000); // simulated delay
    return new Greeting("Hello, " + HtmlUtils.htmlEscape(message.getName()) + "!");
  }

}
 ```

The **@MessageMapping** annotation ensures that, if a message is sent to the /hello destination, the greeting() method is called.

### Configure Spring for STOMP messaging
Create a Java class named **WebSocketConfig**.

**WebSocketConfig** is annotated with @Configuration to indicate that it is a Spring configuration class. It is also annotated with **@EnableWebSocketMessageBroker**. 
As its name suggests, **@EnableWebSocketMessageBroker** enables WebSocket message handling, backed by a message broker.

### Create a Browser Client
This HTML file imports the SockJS and STOMP javascript libraries that will be used to communicate with server through STOMP over websocket.  also import app.js, which contains the logic of client application. 
