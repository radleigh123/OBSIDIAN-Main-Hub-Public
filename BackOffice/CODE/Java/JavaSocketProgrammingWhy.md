---
cssclass:
aliases:
tags:
- Java
- 
---
**[[Java#Network Programming|HOME [Java]]]**

---
## Why Use Sockets?
Why even use manual socket programming if you can easily establish inter-computer communication with, say, HTTP-based protocol (it uses sockets internally), start one of many open-source or commercial web servers, and have clients connect to the server as shown in the preceding sample programs in this lesson? Because a socket connection has a lot less overhead than any standard protocol.

You can create your own very compact protocol that will allow you to send only the data you need, with no or minimal headers. Socket communication provides a duplex byte stream, whereon the data travels simultaneously in both directions, unlike protocols based on the request-response model. Think of financial trading systems: Speed is the king there, and the ability to send data up and down at the same time saves milliseconds, which makes a difference.

On the other hand, if you design your application to use sockets, the live connection will be maintained for each user connected to `ServerSocket`. If your program has to maintain several thousand concurrent connections it will require more powerful servers than programs using the request-response system, with which a connection is maintained only during the time of the client’s request.

<br>

# 
---
- [[JavaSocketProgrammingELI5|ELI5Sockets]]