---
cssclass:
aliases:
tags:
- Java
- 
---
**[[UpdateJava#Processing E-mail w/ Java|HOME [Java]]]**

---
People send and receive e-mails using e-mail client programs such as Microsoft Outlook and Gmail. Can you write your own program to send and receive e-mails? The chances are slim that you’ll need to develop a client to compete with Gmail, but enterprise Java applications often need the ability to send or receive e-mails in certain conditions.

For example, an application that processes credit card transactions suspects a fraudulent activity and needs to send an e-mail to the account owner. Such an application becomes an e-mail client. A Java application provided by your bank can run on your Android smartphone and have an integrated e-mail inbox that accumulates all messages sent to you by the bank.

Another good example involves the forgotten-password functionality. A user clicks the Forgot Your Password? hyperlink and enters a valid e-mail address in a text input field. A couple of seconds later an e-mail containing instructions for resetting the password arrives in her e-mail inbox. The server-side Java program sent this e-mail automatically using `JavaMail`’s application program interface (API). In this lesson you’ll learn how to write a Java program that can send e-mails reminding you about your friends’ birthdays.

## Protocols and Servers
For e-mail messaging you’ll be using standard protocols: Simple Mail Transfer Protocol (SMTP) for sending e-mails and Post Office Protocol (POP) or Internet Message Access Protocol (IMAP) for retrieving e-mails. The third version of this protocol is called POP3; IMAP is a more advanced alternative to POP3. The format of the message body and its attachments, if any, is defined by the Multipurpose Internet Mail Extensions (MIME) protocol.

Some vendors use proprietary protocols for e-mails, but we’ll stick to standards. For Java SE, JavaMail API is an optional package that has to be downloaded separately, but it is included with Java EE. The API is simple to use — it takes only a few lines of code to send an e-mail from a Java program.

To test a client program that sends e-mails you’ll need to know the hostname and port of some SMTP server and have an account with the service provider. Typically such servers use port 25 or 587 for e-mails encrypted using Transport Layer Security (TLS) protocol and port 465 for Secure Sockets Layer (SSL) encryption. Some ISPs may block these ports though.

Apart from an SMTP server hosted by your ISP, you can use the free public server smtp.gmail.com offered by Google. For the parameters of this server refer to the following Web page: http://mail.google.com/support/bin/answer.py?hl=en&answer=13287. Yahoo! also offers a free public SMTP server at smtp.mail.yahoo.com.

Here’s a word of caution: After you learn how easy it is to write a Java program that sends e-mails, you might have an urge to start sending mass e-mails to large lists of recipients to promote your business or share the latest jokes you’ve found online. Unsolicited e-mail is called spam, and if you write a program that sends dozens of e-mails per minute your ISP will probably notice it and give you a warning or even terminate your Internet access.