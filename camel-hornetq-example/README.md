# camel-hornet-spring-example

This is an example Maven project which shows how to connect Camel and HornetQ using Spring.

Its pretty much [this](http://integrationsphere.blogspot.ca/2011/07/camel-and-hornetq-as-jms-provider.html) blog post made to work in Eclipse Juno.

## Prerequisites
 - a standalone HornetQ instance running locally
 - a way to publish to a jms queue and subscribe to a jms topic
 
## Running

Build the project in Eclipse, the console should spit out a few lines and then sit doing nothing.

 - subscribe to the jms topic 'helloworld'
 - publish a message to the jms queue 'inputqueue'
 
The message published to the queue should appear on the topic subscriber output. The Camel route defined in the Spring context is successfully mapping the published message to the subscriber queue.

## Debugging

The Maven pom.xml has a reference to the name of the project, this'll need to be updated to the name you have for any project that may have been copied from this one.

You may need to fiddle with the build configuration for the project. This is intended to run as a Java Application, search for the main class and use the Spring one that is one of those found.