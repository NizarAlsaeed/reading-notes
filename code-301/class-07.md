# APIs continued
Application Programming Interface (API)
An API is different from a database backed (or static) web application or site in that it does not generally need to contain a frontend, Requests to retrieve or write data are generally done without a frontend, by sending an HTTP request to a server.

In order to build a public API, you’ll need the following:

1. A backend with routing of requests and responses
2. A database where your application can store its data. 
3. A server, that is accessible to the internet, where your application can run.



## REST
The world wide web is built on an architectural style called “REST”or “REpresentational State Transfer”. REST provides a definition of a “resource”, A web page is a “representation” of a resource.

when you go to a web page, the browser does an HTTP GET on the URL you type in and back comes a web page.browser goes and GETs using the HTTP protocol on all the resources untill the web page is displayed.