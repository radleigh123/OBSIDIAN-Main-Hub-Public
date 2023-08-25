---
cssclass:
aliases:
tags:
- Java
- Java/Applets
---
**[[Java#Java Applets (deprecated)|HOME [Java]]]**

---
## Restrictions of Java Applets
$\qquad$People browse the Internet without knowing if web pages contain Java applets or not, but they want to be sure that the files located in their computers will not be harmed by some bad guys who have added a nasty applet to a page. **Unsigned applets** are the ones that haven’t gone through a special *signing process* to obtain a security certificate indicating that they come from a trusted source.

**Unsigned** (aka *untrusted*) Java applets operate inside a so-called *security sandbox* and have the following main restrictions:
- They can’t access local files on your disk.
- They can connect only to the computer they were downloaded from.
- They can’t start any other programs located in your computer.

Applets can be signed by ***VeriSign*** or ***Thawte*** and operate outside the security sandbox and be unrestricted in their ability to access the user’s computer if the user accepts the applet’s security. A **signed applet** will run outside the security sandbox. If the user refuses to accept the certificate, the applet will run within the security sandbox as unsigned.

To run an applet you’ll need a Java class written in a special way, an HTML text file that contains the tag `<applet>` pointing to this class, and a web browser that supports Java. You can also test applets in Eclipse or using a special program called **appletviewer**. One must have knowledge about [[HTML]] to be able to make applets.