---
cssclass:
title: JavaNetworkProxyServers
creation-date: 2023-04-16
aliases:
tags:
- Java
- Java/java.net
- Java/Proxy
---
**[[Java#Network Programming|HOME [Java]]]**

---
## Connecting through HTTP Proxy Servers
For security reasons, most enterprises use *firewalls* (see <u>http\://en.wikipedia.org/wiki/ Firewall_%28computing%29</u>) to block unauthorized access to their internal networks. As a result their employees can’t directly reach the outside Internet world (or even some internal servers), but go through **HTTP proxy servers**.

A regular Java application should specify the `http.proxyHost` and `http.proxyPort` parameters to “*drill a hole*” in the firewall. For example, if the name of your proxy server is `proxy.mycompany.com` and it runs on `port 8080`, the following two lines should be added to your Java application that needs to connect to the Internet:
```java
System.setProperty(“http.proxyHost”,”http://proxy.mycompany.com”);
System.setProperty(“http.proxyPort”, 8080);
```
If you do not want to hardcode these values, pass them to your program from the command line:
```cmd
java -Dhttp.proxyHost=http://proxy.mycompany.com 
	–Dhttp.proxyPort=8080 WebSiteReader
```
The other option for programmatically specifying proxy parameters is to do it via the class `java.net.Proxy`. The code for the same proxy server parameter would look like this (you can replace the name of the server with an IP address):
```java
Proxy myProxy = new Proxy(Proxy.Type.HTTP, new InetSocketAddress (“http://proxy.mycompany.com”, 8080);
url = new URL(“http://www.google.com/index.html” );
urlConn = url.openConnection(myProxy);
```

<br>

# 
---
- [Proxy (Java Platform SE 7)](https://docs.oracle.com/javase/7/docs/api/java/lang/reflect/Proxy.html)
- https://www.javatpoint.com/java-http-proxy-server