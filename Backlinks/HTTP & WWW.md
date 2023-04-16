---
aliases:
tags:
---
**[[Protocol Stacks1|BACK]]**

---
## HTTP (Hypertext Transfer Protocol) and World Wide Web
One of the most commonly used services on the Internet is the **World Wide Web** (WWW). The application protocol that makes the web work is **Hypertext Transfer Protocol** or **HTTP**. 
>[!BUG|no-i alt-co] Do not confuse this with the Hypertext Markup Language (HTML). **[[HTML]]** is the language used to write web pages.

HTTP is the <mark class="hltr-lightgreen">protocol that web browsers and web servers use to communicate with each other</mark> over the Internet. It is an application level protocol because it sits on top of the TCP layer in the [[Protocol Stacks|protocol stack]] and is used by specific applications to talk to one another. In this case the applications are web browsers and web servers.
>[!INFO|clean ttl-c no-i collapse] [[HTTPS]] (Hyper Text Transfer Protocol Secure) - all data sent back/forth is encrypted.

HTTP is a connectionless text based protocol. Clients (web browsers) send requests to web servers for web elements such as web pages and images. After the request is serviced by a server, the connection between client and server across the Internet is disconnected. A new connection must be made for each request. Most protocols are **connection oriented**. This means that the two computers communicating with each other keep the connection open over the Internet. HTTP does not however. Before an HTTP request can be made by a client, a new connection must be made to the server.

>[!column|no-i collapse] HTTP Status Codes
>>[!INFO|clean no-t]
>> **100-199: Informational**
>> Request received/processing
>> &nbsp;
>> **2xx: Success**
>> Successfully received, understood and accepted
>> &nbsp;
>> **3xx: Redirect**
>> Further action must be taken/redirect
>> &nbsp;
>> **4xx: Client Error**
>> Request does not have what it needs
>> &nbsp;
>> **5xx: Server Error**
>> Server failed to fulfill an apparent valid request
>
>>[!INFO|bg-gray no-t]
>> **200** - OK
>> **201** - OK created
>> &nbsp;
>> **301** - Moved to new URL
>> **304** - Not modified
>> &nbsp;
>> **400** - Bad request
>> **401** - Unauthorized
>> **404** - Not found
>> &nbsp;
>> **500** - Internal server error

<br>

**An upgrade of HTTP/1.1**
![[HTTP2.png|wtall center]]

---
>[!EXAMPLE|no-i ttl-c]- When you type a URL into a web browser, this is what happens:
>1. If the [[URL]] contains a [[domain name]], the browser first connects to a domain name server and retrieves the corresponding [[Internet Address|IP address]] for the web server.
>2. The web browser connects to the web server and sends an HTTP request (via the protocol stack) for the desired web page.
>3. The web server receives the request and checks for the desired page. If the page exists, the web server sends it. If the server cannot find the requested page, it will send an HTTP `404` error message. (`404` means '*Page Not Found*' as anyone who has surfed the web probably knows.)
>4. The web browser receives the page back and the connection is closed.
>5. The browser then parses through the page and looks for other page elements it needs to complete the web page. These usually include images, applets, etc.
>6. For each element needed, the browser makes additional connections and HTTP requests to the server for each element.
>7. When the browser has finished loading all images, applets, etc. the page will be completely loaded in the browser window.

Most Internet protocols are specified by Internet documents known as a **Request For Comments** or **RFC**s. RFCs may be found at several locations on the Internet. HTTP version 1.0 is specified by RFC 1945.

<br>

# 
---
- **RFC** - [Internet RFC/STD/FYI/BCP Archives Search (faqs.org)](http://www.faqs.org/rfcs/rfcsearch.html)