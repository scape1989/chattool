# Getting started

This repository is a netbeans project. If opened in netbeans it should run "out of the box"

If the jar file is run without any command line parameters it will show a GUI that lets you choose whether to run the server or the client functionality.


## Starting the server

To start the server, use ```java -jar "chattool.jar SERVER``` 

The server will listen for incoming connections on port 20000

To change this, use ```java -jar "chattool.jar SERVER  %PORTNUMBER%```  where %PORTNUMBER% is the portnumber


## Starting the client

To start a client from the commandline you need to specify the IP address and port number to connect to

```java -jar "chattool.jar" CLIENT localhost 20000```

It is also possible to start clients (locally) from the GUI by selecting the button "Additional Client" 



## Speeding up testing cycle of conversation controller objects

The process of starting servers and clients is quite tedious for developing. To get round this you can start any Conversation Controller object, along with the required number of clients by using the following syntax:

```
javac -jar "chatool.jar" nogui_ccname_autologin CONVERSATIONCONTROLLERNAME
```

For example:

```java
javac -jar "chatool.jar" nogui_ccname_autologin DyadicTurnByTurnInterface
```

This will automatically start the chattool, load the ConversationController object, initialize the clients and log them in

The default number of clients to start is 2 (which is specified in 
```Configuration.defaultGroupSize```

These can be saved in netbeans project configurations
