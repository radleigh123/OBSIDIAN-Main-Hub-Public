---
cssclass:
aliases:
tags:
- Java
- 
---
**[[UpdateJava#Processing E-mail w/ Java|HOME [Java]]]**

---
## Open Source Components
Apache Commons is a community project that offers a number of open-source reusable components. One of the libraries contains classes for sending and receiving e-mails form Java. You can read about this project at http://commons.apache.org/email/userguide.html. 

The process of sending a simple e-mail with this library comes down to creating an instance of one class, `SimpleEmail`. Then you need to set the properties of this object: host, port, from, to, authenticator, subject, and message body. When this is done, just call the send() method. If all you need is to send simple e-mails, the benefits of using the Apache Commons e-mail library may not be so obvious. But if your program needs to send multipart e-mails with attachments, or HTML-formatted e-mails, consider using this library. One useful feature of this library is that it gives you the ability to specify an alternative recipient for bounced e-mails.

There is one more community project to consider: Apache Velocity (http://velocity.apache.org/). Imagine that you need to write a program that will perform mass mailing of pre-formatted letters, inserting customer-specific information (such as name and address) into each one. The Apache Velocity project would be quite handy for this purpose. It is also useful if you want to send automatic account registrations or password-change e-mails. Instead of hard-coding the letter text into your Java program, you can create text fi les (templates) containing special markup to be substituted with real values by your Java program during run time.

For further details, read the user guide at the following URL: http://velocity.apache.org/engine/devel/user-guide.html. Third-party libraries (e.g. Spring Framework, discussed in Lesson 35) hide specific of the use of `JavaMail` API. Check out the documentation on using e-mails with the Spring Framework at the following URL: http://static.springsource.org/spring/docs/2.0.x/reference/mail.html.