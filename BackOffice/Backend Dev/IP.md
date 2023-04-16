---
aliases:
tags:
---
**[[Internet|BACK]]**

---
## IP (Internet Protocol)
> rules that govern how information is sent from on PC to another PC over an Internet connection.
> $\quad$▪ Public IP Address - accessible over the Internet.
> $\quad$▪ Private IP Address - assigned to a device on a close network such as home or business network, **not accessible over the Internet**.

Unlike [[TCP]], **IP is an unreliable, connectionless protocol**. IP doesn't care whether a packet gets to it's destination or not. Nor does IP know about connections and port numbers. **IP's job is too send and route packets to other computers**. IP packets are independent entities and may arrive out of order or not at all. It is TCP's job to make sure packets arrive and are in the correct order. About the only thing IP has in common with TCP is the way it receives data and adds it's own IP header information to the TCP data. The IP header looks like this:

![[Internet Protocol.png|center wm-tl]]

Above we see the IP addresses of the sending and receiving computers in the IP header. Below is what a packet looks like after passing through the application layer, TCP layer, and IP layer. The application layer data is segmented in the TCP layer, the TCP header is added, the packet continues to the IP layer, the IP header is added, and then the packet is transmitted across the Internet.

![[Internet Protocol1.png|center wm-tl]]

<br>

# 
---
- 