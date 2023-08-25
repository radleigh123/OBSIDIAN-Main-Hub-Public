---
cssclass:
title: JavaNetworkProgramming
creation-date: 2023-04-14
aliases:
tags:
- Java
---
**[[Java#Network Programming|HOME [Java]]]**

---
# Network Programming
Computers connected to a network can communicate with each other only if they agree on the rules of communication, called [[IP|protocol]], that define how to request the data, if the data should be sent in pieces, how to acknowledge received data, if the connection between two computers should remain open, and so on. ([[TCP]]/[[Internet Address]]), ([[UDP]]/IP), [[FTP]], and [[HTTP & WWW]] are some examples of network protocols.

[[LAN|Local area network]] (LAN) refers to a computer network connecting devices in a small area — the same office or house, or a rack. Interconnected computers located farther apart or that belong to different companies are part of a [[LAN#^658c1d|wide area network]] (WAN). The [[HowInternetWorks|Internet]] consists of millions of networks and individual devices. When connected networks belong to the same organization it is referred to as an **intranet**. For security reasons intranets are shielded from the rest of the world by special software called **firewalls**.

The [[HTTP & WWW|World Wide Web]] (WWW) uses uniform resource locators ([[URL]]s) to identify online resources.
> For example, the following URL says that there is (or will be generated on the fly) a file called `training.html` located at the remote host known as `mycompany.com`, and that the program should use the HTTP protocol to request this file. It also states that this request has to be sent via `port 80`.
> ```
> www.mycompany.com:80/training.html
> ```

The hostname must be unique and it is automatically converted to the IP address of the physical server by your [[ISP|Internet service provider]] (ISP), aka your *hosting company*. The IP address is a group of four numbers, for example `122.65.98.11`. Most of the individuals connected to the Internet are getting so-called **dynamic** (not permanent) **IP addresses** assigned to their home computers, but for a small extra fee you can request a static IP address that can be assigned to any server located in your basement, office, or garage. In the enterprises, network computers usually get **static** (permanent) **IP addresses**.
>[!FAQ|bg-c-green alt-co] For individual use, it’s sufficient to have a dynamically assigned IP address, as long as your ISP can find your server by resolving a domain name to the current IP address.

Finding a resource online is somewhat similar to finding a person by his or her address. The role of an <mark class="hltr-lightblue">IP address is similar to the role of a street number of a building, and a port plays the role of an apartment number in that building</mark>. Many people can live in the same building, just as many programs can run on the same server.

<center>A <strong>port</strong> is simply a unique number assigned to a server program running on the machine.</center>

Multiple Java technologies exist for providing data exchange among computers in a network. Java provides classes for network programming in the package **java.net**. This chapter shows you how to read data from the Internet using the class URL as well as *direct socket-to-socket programming*. [[Java#Processing E-mail w/ Java|Lesson 19]] is about sending e-mails with `JavaMail API`. [[Java#Java EE 6 Overview|Lessons 26]] through [[Java#Bringing JavaFX to the Mix|Lesson 37]] introduce you to other technologies that you can use over the network: **Java Servlets**, **RMI**, **EJB**, and **JMS**.