---
aliases:
tags:
---
**[[Internet#^SMTP|BACK]]**

---
## SMTP and E-mail
Another commonly used Internet service is **electronic mail**. E-mail uses an application level protocol called **Simple Mail Transfer Protocol** or **SMTP**. SMTP is also a text based protocol, but unlike HTTP, SMTP is connection oriented. SMTP is also more complicated than HTTP. There are many more commands and considerations in SMTP than there are in HTTP.
>[!EXAMPLE|ttl-c no-i]+ When you open your mail client to read your e-mail, this is what typically happens:
>1. The mail client (Netscape Mail, Lotus Notes, Microsoft Outlook, etc.) opens a connection to it's default mail server. The mail server's IP address or domain name is typically setup when the mail client is installed.
>2. The mail server will always transmit the first message to identify itself.
>3. The client will send an SMTP HELO command to which the server will respond with a 250 OK message.
>4. Depending on whether the client is checking mail, sending mail, etc. the appropriate SMTP commands will be sent to the server, which will respond accordingly.
>5. This request/response transaction will continue until the client sends an SMTP QUIT command. The server will then say goodbye and the connection will be closed.

A simple 'conversation' between an SMTP client and SMTP server is shown below. **R:** denotes messages sent by the server (receiver) and **S:** denotes messages sent by the client (sender).
```
This SMTP example shows mail sent by Smith at host USC-ISIF, to
Jones, Green, and Brown at host BBN-UNIX.  Here we assume that
host USC-ISIF contacts host BBN-UNIX directly.  The mail is
accepted for Jones and Brown.  Green does not have a mailbox at
host BBN-UNIX.

-------------------------------------------------------------

	R: 220 BBN-UNIX.ARPA Simple Mail Transfer Service Ready
	S: HELO USC-ISIF.ARPA
	R: 250 BBN-UNIX.ARPA
	
	S: MAIL FROM:<Smith@USC-ISIF.ARPA>
	R: 250 OK
	
	S: RCPT TO:<Jones@BBN-UNIX.ARPA>
	R: 250 OK
	
	S: RCPT TO:<Green@BBN-UNIX.ARPA>
	R: 550 No such user here
	
	S: RCPT TO:<Brown@BBN-UNIX.ARPA>
	R: 250 OK
	
	S: DATA
	R: 354 Start mail input; end with <CRLF>.<CRLF>
	S: Blah blah blah...
	S: ...etc. etc. etc.
	S: .
	R: 250 OK
	
	S: QUIT
	R: 221 BBN-UNIX.ARPA Service closing transmission channel
```
This SMTP transaction is taken from RFC 821, which specifies SMTP.