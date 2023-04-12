---
aliases:
tags:
---
**[[Internet|BACK]]**

---
## The Internet Routing Hierarchy
So how do [[Protocol Stacks|packets]] find their way across the Internet? Does every computer connected to the Internet know where the other computers are? Do packets simply get 'broadcast' to every computer on the Internet? The answer to both the preceding questions is <mark class="hltr-lightred">NO</mark>. No computer knows where any of the other computers are, and packets do not get sent to every computer. The information used to get packets to their destinations are contained in routing tables kept by each router connected to the Internet.

**[[Router|Routers]] are packet switches.** A router is usually connected between networks to route packets between them. Each router knows about it's sub-networks and which [[IP|IP]] addresses they use. The router usually doesn't know what IP addresses are 'above' it. Examine [[Internet Routing Hierarchy.png|Diagram 5]] below. The black boxes connecting the backbones are routers. The larger [[NSP]] backbones at the top are connected at a [[NAP]]. Under them are several sub-networks, and under them, more sub-networks. At the bottom are two local area networks with computers attached.

![[Internet Routing Hierarchy.png|center hs-med]]

When a packet arrives at a router, the router examines the IP address put there by the IP protocol layer on the originating computer. The router checks it's routing table. If the network containing the IP address is found, the packet is sent to that network. If the network containing the IP address is not found, then the router sends the packet on a default route, usually up the backbone hierarchy to the next router. Hopefully the next router will know where to send the packet. If it does not, again the packet is routed upwards until it reaches a NSP backbone. The routers connected to the NSP backbones hold the largest routing tables and here the packet will be routed to the correct backbone, where it will begin its journey 'downward' through smaller and smaller networks until it finds it's destination.