Log service
===========

Introduction
============

The log service provides access to logging service. The implementation
is fully based on the standard logging mechanism introduced in JDK 1.4.

The default access log format follows the [W3C Extended Log File
Format](http://www.w3.org/TR/WD-logfile.html)
with the following fields used:

1.  Date (YYYY-MM-DD)
2.  Time (HH:MM:SS)
3.  Client address (IP)
4.  Remote user identifier (see RFC 1413)
5.  Server address (IP)
6.  Server port
7.  Method (GET|POST|...)
8.  Resource reference path (including the leading slash)
9.  Resource reference query (excluding the leading question mark)
10. Response status code
11. Number of bytes sent
12. Number of bytes received
13. Time to serve the request (in milliseconds)
14. Host reference
15. Client agent name
16. Referrer reference

If you use
[Analog](http://www.analog.cx/)
to generate your log reports, and if you use the default log format,
then you can simply specify this string as a value of the LOGFORMAT
command:
(%Y-%m-%d\\t%h:%n:%j\\t%S\\t%u\\t%j\\t%j\\t%j\\t%r\\t%q\\t%c\\t%b\\t%j\\t%T\\t%v\\t%B\\t%f)

For custom access log format, see the syntax to use and the list of
available variable names in
[Template](http://restlet.org/learn/javadocs/1.1/api/org/restlet/util/Resolver.html#createResolver%28org.restlet.data.Request,%20org.restlet.data.Response%29).

