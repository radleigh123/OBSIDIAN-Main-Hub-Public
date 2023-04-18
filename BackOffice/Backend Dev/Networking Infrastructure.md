---
aliases:
tags:
---
**[[HowInternetWorks#^NETWORKINFRASTRUCTURE|BACK]]**

---
### Network Infrastructure
So now you know how packets travel from one computer to another over the Internet. But what's in-between? What actually makes up the Internet?

![[Networking Infrastructure.png|center wm-tl]] ^0ba957
<center><strong>Diagram 3</strong></center>

The [[ISP]] maintains a pool of modems for their dial-in customers. This is managed by some form of computer (usually a dedicated one) which controls data flow from the modem pool to a backbone or dedicated line router. This setup may be referred to as a [[port server]], as it 'serves' access to the network. Billing and usage information is usually collected here as well.

After your packets traverse the phone network and your ISP's local equipment, they are routed onto the ISP's backbone or a backbone the ISP buys bandwidth from. From here the [[Protocol Stacks#^5ae9a6|packets]] will usually journey through several routers and over several backbones, dedicated lines, and other networks until they find their destination, the computer with address 5.6.7.8. But wouldn't it would be nice if we knew the exact route our packets were taking over the Internet? As it turns out, there is a way...
>[!FAQ|alt-co] traceroute
> it shows the path your packets are taking to a given Internet destination. Traceroute will print out a list of all the routers, computers, and any other Internet entities that your packets must travel through to get to their destination.
> 
> **Windows** - `tracert [domain_name]`
> **Unix** - `traceroute [domain_name]`
> 
>> If you use traceroute, you'll notice that your packets must travel through many things to get to their destination. Most have long names such as `sjc2-core1-h2-0-0.atlas.digex.net` and `fddi0-0.br4.SJC.globalcenter.net`. These are Internet routers that decide where to send your packets.

Several routers are shown in [[Networking Infrastructure#^0ba957|Diagram 3]], but only a few. It is meant to show a simple network structure.

<br>