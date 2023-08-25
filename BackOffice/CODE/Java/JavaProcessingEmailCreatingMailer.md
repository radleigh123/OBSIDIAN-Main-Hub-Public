---
cssclass:
aliases:
tags:
- Java
- 
---
**[[Java#Processing E-mail w/ Java|HOME [Java]]]**

---
## Creating a Birthday Mailer
Because I’ll be writing a birthday mailer program using Java SE, I need to download the jars (libraries) with `JavaMail` classes. At the time of this writing `JavaMail` API 1.4.3 is the latest release, and you can download it from www.oracle.com/technetwork/java/index-138643.html.

Unzip the `JavaMail` archive — it includes all required jar files, demos, and documentation. Create an Eclipse project called Lesson19, right-click the project name, and select Properties฀➪฀Java Build Path. Go to the Libraries tab, click Add External JARs, and add mailapi.jar and smtp.jar to the project from the lib directory of the extracted archive. These jars contain all the classes from the `javax.mail` package required to send e-mails. If you are using a really old version of Java (prior to version 6) you’ll also need to download and add to your project the JavaBeans Activation Framework (JAF).

**Required Supporting Classes**
At a minimum you have to use the following classes to send an e-mail:
- `javax.mail.Session`: This class knows important characteristics of your environment, such as the name of the mail server.
- `javax.mail.Message`: This class represents your message, containing recipients, subject, content, and so on.
- `javax.mail.internet.InternetAddress`: The recipient of your message will be represented by this class.
- `javax.mail.Transport`: This class will pass your message for the delivery to a protocol specific transport.

**Writing the Mail Sender**
Now you’ll learn how to write a program to send e-mail messages. I’ll be using the publicly available SMTP server from Yahoo!, but if you decide to use the server provided by your ISP you can find out its hostname and port from the settings of your current e-mail client program. For example, Microsoft Outlook has this information in the menu Tools฀➪฀Accounts฀➪฀Mail฀➪฀Properties.

Typically SMTP servers require you to provide a valid e-mail address and password for authentication. Because your JavaMail program won’t use a log-on window, you can hard-code e-mail credentials in a subclass of JavaMail’s Authenticator, as shown in Listing 19-1.
```java
import javax.mail.Authenticator;
import javax.mail.PasswordAuthentication;

class MyMailAuthenticator extends Authenticator { 
	protected PasswordAuthentication getPasswordAuthentication() {
	return new PasswordAuthentication ("test@yahoo.com", "password123");
	}
}
```
If `MyMailAuthenticator` isn’t able to authenticate using the provided e-mail/password combination, it’ll throw the `AuthenticationFailedException` with the error message “*Access Denied*.” If you’ll specify a nonexistent sender’s e-mail address, the program will throw `SMTPSendFailedException` with the error “From address not verified.” If authentication is not required, the class `MyMailAuthenticator` is not needed. 

A sample file that stores the birthdays of your e-mail contacts is shown in Listing 19-2. It’s a file in a CSV format, where each line contains the birthday, name, and e-mail address of a contact.
```
Aug-9,Mary Lou,mlou@gmail.com
Mar-31,John Smith,jsmith@gmail.com
Aug-9,David Lee,dlee@yahoo.com
```
The Mailer program (see Listing 19-3) will read this file into an array, and if the birthday’s date is the same as the current date, it’ll send a “happy birthday” e-mail to this person. The program starts by creating an object with the properties of the SMTP server at Yahoo! Then it creates an instance of the `MyMailAuthenticator` class and gives both of them to the Session instance.

When this is done the method main() invokes the method `readBirthdayFile()`, which populates [[JavaArrayList|ArrayList]] friends with the data from the file birthday.txt. Then the method `iterateThroughBirthdays()` parses only those lines in which the birthday date is the same as the current date. This program uses the class `java.util.Scanner`, which parses the content of the String (the friend’s data) based on specified delimiters. The `setPropsAndSendEmail()` method has the code for sending e-mails. First it creates an instance of the Message object and populates it with all the familiar parameters: from, recipient(s), subject, data, and the text of the message. The call to `Transport.send()` performs the actual process of sending this message.
```java
import java.io.*;
import java.text.*;
import java.util.*;
import javax.mail.*;
import javax.mail.internet.*;

public class Mailer {
	private Session session = null;
	private static String emailSenderAddress = "yfain11@yahoo.com";
	private static String emailSubject = "Happy Birthday!!!";
	private String emailText = "Happy birthday dear %s!!!";
	ArrayList<String> friends = new ArrayList<String>();
	
	Mailer() {
		Properties sessionProperties = new Properties();
		sessionProperties.put("mail.smtp.host", "smtp.mail.yahoo.com");
		sessionProperties.put("mail.smtp.user", emailSenderAddress);
		sessionProperties.put("mail.smtp.port", "25");
		sessionProperties.put("mail.smtp.auth", "true");
		
		MyMailAuthenticator authentificatorForMessage = new MyMailAuthenticator();
		session = Session.getInstance(sessionProperties, authentificatorForMessage);
	}
	
	private void setPropsAndSendEmail(String emailRecipient, String emailText){
		try{
			Message emailMessage = new MimeMessage(session);
			emailMessage.setFrom(new InternetAddress(emailSenderAddress));
			emailMessage.setRecipients(Message.RecipientType.TO, InternetAddress.parse(emailRecipient, false));
			emailMessage.setSubject(emailSubject);
			emailMessage.setSentDate(new Date());
			emailMessage.setText(emailText);
			Transport.send(emailMessage);
			System.out.println("Your email to " + emailRecipient + " has been sent successfully");
		}catch(Exception e){
			System.out.println("Your email to " + emailRecipient + " has not been sent: " + e.getMessage());
			e.printStackTrace();
		}
	}
	
	private void readBirthdayFile() throws IOException {
		FileInputStream birthdayFile = new FileInputStream("birthday.txt");
		BufferedReader birthdayFileReader = new BufferedReader(new InputStreamReader(birthdayFile));
		
		String friendInfo;
		
		while ((friendInfo = birthdayFileReader.readLine()) != null){
			friends.add(friendInfo);
		}
		
		birthdayFileReader.close();
		birthdayFile.close();
	}
	
	private void iterateThroughBirthdays(){
		Iterator<String> iterator = friends.iterator();
		
		while (iterator.hasNext()){
			scanForManInfoAndSendEmail(iterator.next());
		}
	}
	
	private void scanForManInfoAndSendEmail(String stringFromArray){
		Scanner scannerOfLines = new Scanner(stringFromArray).useDelimiter("[,\n]");
		
		if (scannerOfLines.next().equals(getCurrentDateMMMd())) {
			String emailAddressee = scannerOfLines.next();
			String emailAddress = scannerOfLines.next();
			setPropsAndSendEmail(emailAddress, 
			String.format(emailText, emailAddressee));
		}
	}
	
	private static String getCurrentDateMMMd(){
		return new SimpleDateFormat("MMM-d", Locale.US).format(new GregorianCalendar().getTime());
	}
	
	public static void main(String[] args){ 
		Mailer mm = new Mailer();
		
		try {
			mm.readBirthdayFile();
			mm.iterateThroughBirthdays();
		} catch (IOException e) {
			e.printStackTrace();
		}
	}
}
```