---
aliases:
tags:
---
**[[Internet|BACK]]**

---
## Domain Names & Address Resolution
But what if you don't know the [[IP]] address of the computer you want to connect to? What if the you need to access a web server referred to as <u>*www.anothercomputer\.com*</u>? How does your web browser know where on the Internet this computer lives? The answer to all these questions is the [[DNS|Domain Name Service]] or **DNS**. The DNS is a distributed database which keeps track of computer's names and their corresponding IP addresses on the Internet.

Many computers connected to the Internet host part of the DNS database and the software that allows others to access it. These computers are known as DNS servers. If a DNS server does not contain the domain name requested by another computer, the DNS server re-directs the requesting computer to another DNS server.
> No DNS server contains the entire database; they only contain a subset of it.

![[Domain Name.png|center hs-med]]

The Domain Name Service is structured as a hierarchy similar to the IP routing hierarchy. The computer requesting a name resolution will be re-directed 'up' the hierarchy until a DNS server is found that can resolve the domain name in the request. The image above illustrates a portion of the hierarchy. At the top of the tree are the domain roots. Some of the older, more common domains are seen near the top. What is not shown are the multitude of DNS servers around the world which form the rest of the hierarchy.

When an Internet connection is setup (e.g. for a [[LAN]] or Dial-Up Networking in Windows), one primary and one or more secondary DNS servers are usually specified as part of the installation. This way, any Internet applications that need domain name resolution will be able to function correctly. For example:
$\quad$ 1️⃣ when you enter a web address into your web browser;
$\quad$ 2️⃣ the browser first connects to your primary DNS server;
$\quad$ 3️⃣ after obtaining the IP address for the domain name you entered;
$\quad$ 4️⃣ the browser then connects to the target computer and requests the web page you wanted.

>[!EXAMPLE]- Try it out
> If you're using Windows 95/NT and access the Internet, you may view your DNS server(s) and even disable them.
> &nbsp;
> <u>If you use Dial-Up Networking:</u>
> Open your Dial-Up Networking window (which can be found in Windows Explorer under your CD-ROM drive and above Network Neighborhood). Right click on your Internet connection and click Properties. Near the bottom of the connection properties window press the TCP/IP Settings... button.
> &nbsp;
> <u>If you have a permanent connection to the Internet:</u>
> Right click on Network Neighborhood and click Properties. Click TCP/IP Properties. Select the DNS Configuration tab at the top.
> &nbsp;
> You should now be looking at your DNS servers' IP addresses. Here you may disable DNS or set your DNS servers to 0.0.0.0. (Write down your DNS servers' IP addresses first. You will probably have to restart Windows as well.) Now enter an address into your web browser. The browser won't be able to resolve the domain name and you will probably get a nasty dialog box explaining that a DNS server couldn't be found. However, if you enter the corresponding IP address instead of the domain name, the browser will be able to retrieve the desired web page. (Use ping to get the IP address prior to disabling DNS.) Other Microsoft operating systems are similar.