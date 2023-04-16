---
aliases:
tags:
---
**[[Internet|BACK]]**

---
## TCP (Transmission Control Protocol)
> Under the application layer in the protocol stack is the TCP layer. When applications open a connection to another computer on the Internet, the messages they send (using a specific application layer protocol) get passed down the stack to the TCP layer.

<mark class="hltr-lightgreen">TCP is responsible for routing application protocols to the correct application on the destination computer</mark>. To accomplish this, port numbers are used. Ports can be thought of as separate channels on each computer. For example, you can surf the web while reading [[SMTP|e-mail]]. This is because these two applications (the web browser and the mail client) used different port numbers. When a [[Protocol Stacks|packet]] arrives at a computer and makes its way up the [[protocol stacks]], the TCP layer decides which application receives the packet based on a port number.
>[!EXAMPLE]+ TCP works like this:
>- When the TCP layer receives the application layer protocol data from above, it segments it into manageable 'chunks' and then adds a TCP header with specific TCP information to each 'chunk'. The information contained in the TCP header includes the port number of the application the data needs to be sent to.
>- When the TCP layer receives a packet from the IP layer below it, the TCP layer strips the TCP header data from the packet, does some data reconstruction if necessary, and then sends the data to the correct application using the port number taken from the TCP header.
> 
> This is how TCP routes the data moving through the protocol stack to the correct application.

TCP is not a textual protocol. **TCP is a connection-oriented, reliable, byte stream service**. Connection-oriented means that two applications using TCP must first establish a connection before exchanging data. TCP is reliable because for each packet received, an acknowledgement is sent to the sender to confirm the delivery. TCP also includes a checksum in it's header for error-checking the received data. The TCP header looks like this:

![[TCP.png|center wm-tl]]

Notice that there is no place for an IP address in the TCP header. This is because TCP doesn't know anything about IP addresses. TCP's job is to get application level data from application to application reliably. The task of getting data from computer to computer is the job of IP.

![[TCP1.png|center wm-tl]]

<br>

# 
---
- 