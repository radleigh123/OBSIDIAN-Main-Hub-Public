---
cssclass:
title: JavaSocketProgramming
creation-date: 2023-04-24
aliases:
tags:
- Java
- Java/Socket
- Java/ServerSocket
---
**[[UpdateJava#Network Programming|HOME [Java]]]**

---
# Socket Programming
Java-based technologies offer many options for network communications, and one of the technologies to consider is **sockets**. In this section you learn how to use the Java classes `Socket` and `ServerSocket` from the package java.net.
> A socket is a connection end point in IP networking. TCP/IP protocol maintains a socket connection for the whole period of communication, while UDP is a connectionless protocol, which sends data in small chunks called datagrams.

The socket address is a pair: IP address and port. When a Java program creates an instance of the `ServerSocket` class, this instance becomes a server that just runs in memory and listens on the specified port for other program requests. The following lines create a server that is listening to `port 3000`:
```java
ServerSocket serverSocket = new ServerSocket(3000);
client = serverSocket.accept();
```

The client program should create a client socket — an instance of the class `Socket` — pointing at the computer/port on which the `ServerSocket` is running. The client program can connect to the server using hostnames or IP addresses too, for example:
```java
clientSocket = new Socket(“124.67.98,101”, 3000);
clientSocket = new Socket(“localhost”, 3000);
clientSocket = new Socket(“127.0.0.1”, 3000);
```

While deciding which port number to use for the `ServerSocket`, avoid using port numbers below `1024` to avoid conflicts with other system programs. For example, 
$\quad$▪ `port 80` is typically used by HTTP servers;
$\quad$▪ `port 443` is reserved for HTTPS;
$\quad$▪ `port 21` is typically used for FTP communications;
$\quad$▪ `port 389` is for LDAP servers, and so on.

After creating a socket-based connection, both client and server should obtain references to its input/output streams and use them for data exchange.

<br>

# 
---
- [[JavaSocketProgrammingWhy|Why use sockets?]]