---
cssclass:
aliases:
tags:
- Java
- 
---
**[[Java#Processing E-mail w/ Java|HOME [Java]]]**

---
## How to Retrieve Emails
Even though more often than not the receivers of the messages sent by a Java application will use one of the popular e-mail clients already available, you may need to incorporate message-retrieving functionality into your application. In this section I’ll just give an overview of the process of retrieving e-mails programmatically, and in the “Try It” section you’ll write such a program on your own.

As in your local post office, incoming mail should be stored somewhere. The POP3 or IMAP mail server provides such storage. POP3 is an older protocol that retrieves messages from a single mailbox. IMAP is newer and more advanced: It allows the organization of messages in folders with filtering support.

To get access to the user’s incoming e-mails the Java program needs to connect to the mail server and get an instance of the Store object by calling the method `getStore()` on the Session object.

You’ll need to know the hostname of your mail server, the protocol it uses, and the relevant user ID and password in order to get the Store instance.

The next step is establishing a connection with Store by calling its method connect(). After this is done, get store’s default root folder and then a specific sub-folder, such as INBOX.

Folders in `JavaMail` are represented by the class Folder. Its method open() will open the specified folder for READ_ONLY or READ_WRITE. Finally, the `getMessages()` method returns an array of Message objects. Iterating through this array will allow you to retrieve message data by calling `getSubject()`, `getFrom()`, `getContent()`, and so on.

Listing 19-4 shows a fragment of the code for retrieving messages from a Gmail account. To enable or disable the IMAP or POP protocol, go to Setting฀➪฀Forwarding POP/IMAP in your Gmail client.

**Fragment of code for e-mail retrieval from Gmail**
```java
	Properties properties = System.getProperties(); 
	Session session = Session.getDefaultInstance(properties);
	
	String host = “pop.gmail.com”; // or “imap.gmail.com”
	String username = “yakov”;
	String password = “mypasswd”;
	Store store = session.getStore(“pop3s”); // or “imap”
	store.connect(host, username, password);
	
	Folder rootFolder = popStore.getDefaultFolder();
	defaultPopFolder = defaultPopFolder.getFolder(“INBOX”);
	defaultPopFolder.open(Folder.READ_ONLY);
	
	Message[] message = folder.getMessages();
	for (int i = 0; i < message.length; i++) {
		// get message parts here 
	}
```
`JavaMail` has full support for multipart messages with attachments (see the `Multipart`, `MimeMultipart`, and `MimeBodyPart` classes), but multipart message support is beyond the scope of this book. The description of these classes is available in the Java help system. Look for these class descriptions in the package `javax.mail`.