---
aliases:
tags:
---
**[[Internet|BACK]]**

---
### Internet Address
>[!CITE|alt-co] the Internet must have a **unique address**

- also known as an **[[IP]]** address
- are in the form *nnn.nnn.nnn.nnn* where *nnn* must be a number from 0 - 255.

![[Internetimage0.png|center]]
<center>two computers connected to the Internet; your computer with IP address 1.2.3.4</center>
<center>and another computer with IP address 5.6.7.8.</center>


If you connect to the Internet through an **[[ISP]]**, you are usually assigned a temporary IP address
If you connect to the Internet from a **[[LAN]]** your computer might have a permanent IP address or it might obtain a temporary one from a **[[DHCP|DHCP server]]**.

In any case, if you are connected to the Internet, your computer has a unique IP address.

>[!FAQ]+ **ping**
>> a handy program to see if a computer on the Internet is alive
> 
> The ping program will send a `ping` (actually an **ICMP** (*Internet Control Message Protocol*) echo request message) to the named computer. The pinged computer will respond with a reply. The ping program will count the time expired until the reply comes back (if it does). Also, if you enter a domain name (i.e. *www\.yahoo\.com*) instead of an IP address, ping will resolve the domain name and display the computer's IP address. More on [[Domain Name|domain names]] and address resolution later.
> 
> **Windows** - `ping [domain_name]`
> **Unix** - same

<br>