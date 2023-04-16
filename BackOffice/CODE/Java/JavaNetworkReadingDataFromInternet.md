---
cssclass:
title: JavaNetworkReadingDataFromInternet
creation-date: 2023-04-14
aliases:
tags:
- Java
- Java/java.io
- Java/java.net
- Java/URL
---
**[[UpdateJava#Network Programming|HOME [Java]]]**

---
# Reading Data from the Internet
You learned in [[UpdateJava#Working with Streams|Lesson 16]] that to read local file streams, a program has to specify the file’s location, such as `c:\practice\training.html`. The same holds true for reading remote files — the only difference is that you open the stream over the network. Java has a class, `java.net.URL`, that will help you to connect to a remote computer on the Internet and get access to a resource there, provided that it’s not protected from the public.

Creation of the `URL` object does not establish a connection with the remote machine; you’ll still need to open a stream and read it. Perform the following steps to read a file from the Internet:
1. Create an instance of the class `URL`. 
2. Create an instance of the `URLConnection` class and open a connection using the `URL` from 
Step 1. 
3. Get a reference to an input stream of this object by calling the method `URLConnection.getInputStream()`.
4. Read the data from the stream. Use a buffered reader to speed up the reading process.

While using streams over the networks you’ll have to handle possible I/O exceptions the way you did while reading the local files. The server you are trying to connect to has to be up-and-running and, if you’re using HTTP-based protocols, a special software - [[Web Server|web server]] - has to be “listening to” the specified port on the server. By default, web servers are listening to all [[HTTP & WWW]] requests on port 80 and to secure HTTPS requests directed to `port 443`.
- [[JavaNetworkReadingDataFromInternetSample0|Sample program that reads contents of an existing generated file]]

The class `WebSiteReader` explicitly creates the object `URLConnection`. Strictly speaking, you could achieve the same result by using the class URL:
```java
URL url = new URL(“http://www.google.com”);
InputStream in = url.getInputStream();
Buff= new BufferedReader(new InputStreamReader(in));
```
The reason you may consider using the `URLConnection` class is that it could give you some additional control over the I/O process. For example, by calling its method `setDoOutput(true)` you specify that this Java program is intended to write to the remote URL too. In the case of HTTP connections, this will also implicitly set the type of request to **POST** ([[UpdateJava#Programming w/ Servlets|see Lesson 27]]). The method `useCaches()` of `URLConnection` also allows you to specify whether the protocol can use a cached object or should always request a fresh copy. In general, if you are planning to write Java programs that will work using HTTP protocol, use the class `HttpURLConnection`, which supports HTTP-specific features, such as processing header fields, getting HTTP response codes, setting request properties, and so on.

<br>

# 
---
- https://www.baeldung.com/java-url
- [URL (Java Platform SE 7)](https://docs.oracle.com/javase/7/docs/api/java/net/URL.html)
- https://www.javatpoint.com/URL-class