## Synopsis

A basic http Proxy server built over netty framework. It  processes about 1000 (tested for) requests per second.

## Code Example

Uses Netty framework to asynchronously process requests. 

 asyncHttpClient.prepareGet(request.getUri()).execute(handler).toCompletableFuture().thenApply(response -> {
 }
 
## Installation

Set up requires maven. 

Unzip the Pserver.zip and move to Pserver directory. 

Execute

Execute

** Update the maven dependencies : 
    
    > mvn clean install -U
  
  
** Compile and build  : 

    > mvn compile

** Start the Proxy server 

    > mvn exec:java  -Dexec.mainClass="com.ps.ProxyServer" -Dexec.args="--port 8080"

 
     --port : port where the proxy server listens for request.
     
     --help : gives usage 
 
## Tests

 using Curl :

example : curl --verbose -x localhost:8080 -X GET www.cnn.com

OR

Set up proxy using browser

Load test using Jmeter

Performance tests using Jmeter on a local server.
 
Test Summary : 
 Writing log file to: /home/kavitha/Jmeter/jmeter.log
 Creating summariser <summary>
 Created the tree successfully using apache-jmeter-3.1/GenReq.jmx
 Starting the test @ Fri Feb 24 00:33:35 PST 2017 (1487925215386)
 Waiting for possible Shutdown/StopTestNow/Heapdump message on port 4445
 summary =  10000 in 00:00:09 = 1164.0/s Avg:   518 Min:     1 Max:  2064 Err:     0 (0.00%)


## Contributors

Reach me at kavitha.lakshmi@gmail.com for any questions.

## License

MIT Copyright (c) 2017

