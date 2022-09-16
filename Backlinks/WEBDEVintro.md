# Introduction How the Web Works
#webdev 

[**Client**](Client.md) | **[Server](Server.md)** 
----   |   ----

## Internet
- ==is a vast network that connects computers all over the world.==
- it works by using a packet routing network that follows:
	- [**IP** (Internet Protocol)](IP.md)
	- [**TCP** (Transport Control Protocol)](TCP.md)

> **The Internet is like a giant library.**

---
## When you type in a Web Address into your browser
1. Your 💻device is connected through a modem or router. which allows it to connect to other networks around the globe.
	- **Modem** - connects to the [ISP](ISP.md)
	- **Router** - allows for multiple computers to join the same network, using the modem

2. Type in a web address, known as a URL, into your browser.
	- [**URL** (Uniform Resource Locator)](URL.md)

3. Your query is processed and pushed to your [ISP](ISP.md) which connects to several servers that store and send data:
	- [**DNS** (Domain Server Server)](DNS.md)
		- Next, your browser looks up the [IP](IP.md) address for the domain name you typed into your search engine through DNS.
	- [**NAP** (Network Access Protection)](NAP.md)

4. Your browser sends a HTTP request to the target server to send a copy of the website to the client using [TCP](TCP.md)/[IP](IP.md).
	- [**HTTP** (Hypertext Transfer Protocol)](HTTP.md)
	- [**HTTPS** (Hypertext Transfer Protocol Secure)](HTTPS.md)

5. [Server](Server.md) approves request and sends a “200 OK” message to client computer. Then, the server sends web page files to browser in the form of data packets.

6. Finally, web page loads as your browser reassembles packets.

![[1.jpeg]]

![[2.jpeg]]

![[3.jpeg]]


---
## [Internet Backbone](Internet%20Back.md)
- Submarine Cables
	- ==world’s information super-highways==
	- in comparison with satellites, subsea cables provide high capacity, cost-effective, and reliable connections that are critical for our daily lives.
	- www.submarinecablemap.com


# 
---
**Resource List**
 - [IntroPDF](https://drive.google.com/file/d/1dvDs5SzDasugQaIA1afCobvmSF2IYE2Z/view)
- [StepsInternet](https://www.hp.com/us-en/shop/tech-takes/how-does-the-internet-work#:~:text=It%20works%20by%20using%20a,where%20you%27re%20using%20it.)
- [InfographicInternet](https://imgur.com/a/tQfXE5b)
- [InternetBackbone](https://www.techopedia.com/definition/20115/internet-backbone)
- [Subcablepurpose](https://www.google.com/search?q=submarine+cable+purpose&oq=submarine+cable+purpose&aqs=edge..69i57j0i390l5j69i64.6223j0j1&sourceid=chrome&ie=UTF-8)


**[Home [WEBDEV]](WEBDEV11LEC.md)**