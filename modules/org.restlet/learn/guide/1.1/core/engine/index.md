Restlet Engine
==============

The engine is the set of classes that together supports or implements
the Restlet API. Currently, there is a strict separation with the API,
but this will change in Restlet 1.2 to facilitate the deployment and
packaging of applications.

This seperation will however stay conceptually between the classes that
are expected to be used by Restlet users while developping their
applications and the classes that are expected to be used by the Restlet
core developers.

Note that the engine is also extensible and can detect pluggable
connectors available on the classpath as well as pluggable
authentication helpers.

