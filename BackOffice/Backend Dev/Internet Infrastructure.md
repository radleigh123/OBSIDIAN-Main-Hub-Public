---
aliases:
tags:
---
**[[Internet#^INTERNETINFRASTRUCTURE|BACK]]**

---
## Internet Infrastructure
>[!column|clean no-t collapse]
>>[!INFO|clean ttl-c no-i] Internet Backbone
>> refers to the <mark class="hltr-blue">high-capacity, long-distance data transmission lines</mark> that carry Internet traffic across the world
>> &nbsp
>> &nbsp
>> is made up of a network of high-speed fiber optic cables and other infrastructure that connects the various Internet Service Providers (ISPs) and other networks together
>
>>[!INFO|clean ttl-c no-i] Internet Infrastructure
>> refers to the <mark class="hltr-blue">physical and virtual components</mark> that make up the global network of interconnected computers and devices that we know as the Internet
>> &nbsp
>> includes the fiber optic cables, routers, servers, data centers, and other hardware and software that are necessary to enable data transmission and communication across the Internet

<br>

>[!column|clean no-t collapse]
>>[!INFO|clean ttl-c no-i] Network Service Providers
>> providers typically <mark class="hltr-blue">offer a wider range of communication services beyond just internet access</mark>, such as telephone services, video services, and data services, and they may provide these services over a variety of networks, including wired and wireless networks
>
>>[!INFO|clean ttl-c no-i] Internet Service Providers
>> specifically provide internet access to customers, typically over a wired or wireless network, their <mark class="hltr-blue">primary focus is on providing internet</mark> connectivity

&nbsp
The Internet backbone is made up of many large networks which interconnect with each other. These large networks are known as **[[NSP]]** (**NSP**s). Some of the large NSPs are *UUNet*, *CerfNet*, *IBM*, *BBN Planet*, *SprintNet*, *PSINet*, as well as others. These networks **peer** with each other to exchange packet traffic. Each NSP is required to connect to three **[[NAP|Network Access Points]]** (**NAP**s). At the NAPs, packet traffic may jump from one NSP's backbone to another NSP's backbone. NSPs also interconnect at **[[MAE|Metropolitan Area Exchanges]]** (**MAE**s). 

![[InternetInfrastructureimage.png|center cover]] ^7e18d1
<center><strong>Diagram 4</strong></center>

This picture is only meant to demonstrate how the *NSPs* could interconnect with each other and smaller [[ISP|ISPs]]. None of the physical network components are shown in Diagram 4 as they are in [[Networking Infrastructure#^0ba957|Diagram 3]]. This is because a single NSP's backbone infrastructure is a complex drawing by itself. Most NSPs publish maps of their network infrastructure on their web sites and can be found easily. To draw an actual map of the Internet would be nearly impossible due to it's size, complexity, and ever changing structure.