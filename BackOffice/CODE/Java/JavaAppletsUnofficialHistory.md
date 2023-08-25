---
cssclass:
- justified
aliases:
tags:
- Java
- Java/Applets
---
**[[Java#Java Applets (deprecated)|HOME [Java]]]**

---
## An Unofficial History of Java Applets
$\qquad$Fifteen years ago Netscape’s market share was over 90 percent, but the situation changed when Microsoft introduced Internet Explorer. Back in 1998 there was an infamous lawsuit between Microsoft and Sun Microsystems — the former started quietly introducing its own class library to Java, breaking the write-once-run-anywhere principle of Sun. Sun won that lawsuit. But as the saying goes, it won the battle but lost the war.

Microsoft stopped including the current version of JVM with Internet Explorer. I’m not blaming them for this, but it hurt applets’ popularity — the end user couldn’t just open a web page to see an applet that required, say, JVM version 1.3. The user would need to first download the proper version of JVM, and then only the applets that were written for JVM 1.3 would work. The process of downloading the right JVM plug-in was a multi-step process.

Sun Microsystems showed a lack of competence on the client side, specifically in the area of integration of JVM into web browsers, and Adobe Flash Player, which is also a virtual machine) dominates in this area now.

High penetration of the required run-time environment and the ability to upgrade it easily are crucial for any web-based technology. Adobe Flash Player shines in this area. Flash Player is a virtual machine with a small memory footprint (1.5 Mb), and its installation takes less than 20 seconds after one button click. For years the JVM plug-in was about 16 Mb, and installation was complicated for a non-programmer — it’s a lot smaller now.

This situation changed after the release of Java 6 update 10, which includes the so-called next-generation Java plug-in. Now applets don’t run in the JVM packages with the web browser, but in a separate JVM launched by the Java plug-in. The applet still appears in the web browser’s window, but now it doesn’t depend on the willingness of the browser vendor to include the latest plug-in. You can read more about this next-generation Java plug-in at https://jdk6.dev.java.net/plugin2.

To control the settings of this plug-in in Microsoft Windows, use the Java Control Panel — select Start $\to$ Control Panel $\to$ Java. Under the Advanced tab find the item Java Plug-in where Enable the Next-generation Java Plug-in should be selected by default.

If you run Intel-based MAC OS X 10.6 or above, find out what Java plug-ins are installed by typing "*about:plugins*" into the address bar of your browser. To use the next-generation plug-in on Apple computers follow the instructions at http://blogs.sun.com/thejavatutorials/entry/ enabling the next generation java.

The other major change introduced in the next-generation Java plug-in is the ability to launch Java applets directly from **JNLP** (*Java Network Launch Protocol*) files, which in the previous releases were used only in Java Web Start technology, which allowed local deployment of the applications over the network. As of **Java 10.6.10** you can use the JNLP meta-descriptors to launch applets too. JNLP support is described in detail at www.oracle.com/technetwork/java/javase/index-142562.html.