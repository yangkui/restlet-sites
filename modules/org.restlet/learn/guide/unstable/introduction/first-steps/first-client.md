First client
============

Introduction
============

As we mentioned in the
[introduction](/learn/guide/2.1#/13-restlet/21-restlet.html "Part I - Introduction"),
the Restlet Framework is at the same time a client and a server
framework. For example, you can easily work with remote resources using
its HTTP client connector.

A connector in REST is a software element that enables the communication
between components, typically by implementing one side of a network
protocol. Restlet provides several implementations of client connectors
based on existing open-source projects. The
[connectors](/learn/guide/2.1#/13-restlet/27-restlet/325-restlet/37-restlet.html "Connectors") 
section lists all available client and server connectors and explain how
to use and configure them.

Here we will retrieve the representation of an existing resource and
output it in the JVM console:

~~~~ {.brush: .java}
// Outputting the content of a Web page  
new ClientResource("http://restlet.org").get().write(System.out);  
~~~~

If you are running your client behind a proxy, please [check this
page](/learn/guide/2.0#/13-restlet/27-restlet/325-restlet/37-restlet.html)to
pick an HTTP client that can be configured. The internal HTTP client
doesn't support proxies at the moment.

The next example sets some preferences in your client call, like a
referrer URI:

~~~~ {.brush: .java}
// Create the client resource  
ClientResource resource = new ClientResource("http://restlet.org");  
 
// Customize the referrer property  
resource.setReferrerRef("http://www.mysite.org");  

// Write the response entity on the console
resource.get().write(System.out);  
~~~~

After those first two steps, [let's now develop a more complete Restlet
application](/learn/guide/2.1#/13-restlet/21-restlet/318-restlet/303-restlet.html "First application"),
taking advantage of the various editions of the Restlet Framework.

