---
aliases:
tags:
---
**[[Internet#^PROTOCOLSTACKS|BACK]]**

---
### Protocol Stacks & Packets
Let's say you've dialed into your ISP from home and the message must be transmitted over the phone line. Or...

Let's say your IP address is 1.2.3.4 and you want to send a message to the computer 5.6.7.8. The message you want to send is *"Hello computer 5.6.7.8!"*. Obviously, the message must be transmitted over whatever kind of wire connects your computer to the Internet.

Therefore the message must be translated from alphabetic text into electronic signals, transmitted over the Internet, then translated back into alphabetic text. Every computer needs one to communicate on the Internet and it is usually built into the computer's operating system (i.e. Windows, Unix, etc.). The protocol stack used on the Internet is referred to as the **TCP/IP protocol stack** because of the two major communication protocols used. The TCP/IP stack looks like this:

| **<center>Protocol Layer</center>** | **<center>Comments</center>**                                                                                      |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| Application Protocols Layer         | Protocols specific to applications such as WWW, e-mail, FTP, etc.                                                  |
| Transmission Control Protocol Layer | TCP directs packets to a specific application on a computer using a port number.                                   |
| Internet Protocol Layer             | TCP directs packets to a specific application on a computer using a port number.                                   |
| Hardware Layer                      | Converts binary packet data to network signals and back. (E.g. ethernet network card, modem for phone lines, etc.) | 

If we were to follow the path that the message *"Hello computer 5.6.7.8!"* took from our computer to the computer with IP address 5.6.7.8, it would happen something like this:

![[Internetimage1.png|center cover wm-tl]] ^INTERNETIMAGE1
1. The message would start at the top of the protocol stack on your computer and work it's way downward.
   >[!DONE|alt-co]- Explain:
   > The message starts at the top of the protocol stack on the source computer. This refers to the hierarchy of communication protocols that are used to transmit data over a network. The top of the stack is the application layer, which is responsible for high-level communication between applications and the rest of the stack.
2. If the message to be sent is long, each stack layer that the message passes through may break the message up into smaller chunks of data. This is because data sent over the Internet (and most computer networks) are sent in manageable chunks. On the Internet, these chunks of data are known as **packets**.
   >[!DONE|alt-co]- Explain:
   > If the message is too long, it will be broken up into smaller chunks of data, known as packets. This is because most computer networks, including the Internet, send data in manageable chunks to ensure efficient and reliable transmission. ^5ae9a6
3. The packets would go through the Application Layer and continue to the TCP layer. Each packet is assigned a **port number**. Ports will be explained later, but suffice to say that many programs may be using the [[TCP]]/[[Internet Protocol]] stack and sending messages. We need to know which program on the destination computer needs to receive the message because it will be listening on a specific port.
   >[!DONE|alt-co]- Explain:
   > The packets then move to the TCP (Transmission Control Protocol) layer, where each packet is assigned a port number. Port numbers are used to identify the specific program or application on the destination computer that should receive the message. This is necessary because many programs may be using the TCP/IP stack and sending messages at the same time.
4. After going through the TCP layer, the packets proceed to the IP layer. This is where each packet receives it's destination address, 5.6.7.8.
   >[!DONE|alt-co]- Explain:
   > After passing through the TCP layer, the packets move to the IP (Internet Protocol) layer, where each packet is assigned a destination IP address. The IP address is a unique identifier for each computer on the Internet and helps the packets reach their intended destination.
5. Now that our message packets have a port number and an IP address, they are ready to be sent over the Internet. The hardware layer takes care of turning our packets containing the alphabetic text of our message into electronic signals and transmitting them over the phone line.
   >[!DONE|alt-co]- Explain:
   > The packets are now ready to be sent over the Internet, and the hardware layer takes care of turning the packets into electronic signals that can be transmitted over the phone line.
6. On the other end of the phone line your [[ISP]] has a direct connection to the Internet. The ISPs [[Router]] examines the destination address in each packet and determines where to send it. Often, the packet's next stop is another router.
   >[!DONE|alt-co]- Explain:
   > On the other end of the phone line, the ISP (Internet Service Provider) has a direct connection to the Internet. The ISP's router examines the destination address in each packet and determines where to send it. The packet may pass through multiple routers before reaching its final destination.
7. Eventually, the packets reach computer 5.6.7.8. Here, the packets start at the bottom of the destination computer's TCP/IP stack and work upwards.
   >[!DONE|alt-co]- Explain:
   > When the packets reach the destination computer, they start at the bottom of the destination computer's TCP/IP stack and work upwards. The bottom of the stack is the hardware layer, which is responsible for receiving and decoding the electronic signals into data packets.
8. As the packets go upwards through the stack, all routing data that the sending computer's stack added (such as IP address and port number) is stripped from the packets.
   >[!DONE|alt-co]- Explain:
   > As the packets move up through the stack, all routing information, such as the IP address and port number, that was added by the source computer's stack is stripped from the packets.
9. When the data reaches the top of the stack, the packets have been re-assembled into their original form, "Hello computer 5.6.7.8!"
   >[!DONE|alt-co]- Explain:
   > Finally, when the data reaches the top of the stack, the packets have been reassembled into their original form, and the message can be delivered to the intended program or application on the destination computer. For example, "Hello computer 5.6.7.8!"

<br>