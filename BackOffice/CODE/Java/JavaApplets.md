---
cssclass:
title: JavaApplets
creation-date: 2023-03-17
aliases:
tags:
- Java
- Java/java.applet
- Java/javax.swing
- Java/JApplet
- Java/Applets
---
**[[Java#Java Applets (deprecated)|HOME [Java]]]**

---
# Java Applets
is a special kind of Java program that a browser enabled with Java technology can download from the internet and run. An applet is typically embedded inside a web page and runs in the context of a browser. An applet must be a subclass of the `java.applet.Applet` class. The `Applet` class provides the standard interface between the applet and the browser environment.

[[JavaSwing|Swing]] provides a special subclass of the `Applet` class called `javax.swing.JApplet`. The `JApplet` class should be used for all applets that use Swing components to construct their [[JavaGUI|GUI]].

>[!WARNING|alt-co ttl-c]
> In recent years, major web browsers have started to phase out support for Java applets due to security concerns and other issues.
> &nbsp;
> For example, Google Chrome ended support for Java applets in September 2015, and Mozilla Firefox began limiting support for Java applets in 2016. Oracle, has also deprecated the Java browser plugin, which is required to run Java applets, in more recent versions of Java.

<br>

# 
---
- [Lesson: Java Applets (Oracle)](https://docs.oracle.com/javase/tutorial/deployment/applet/index.html)
- [Java Applets Basics (GeeksforGeeks)](https://www.geeksforgeeks.org/java-applet-basics/)
- [Java Applet Tutorial (javatpoint)](https://www.javatpoint.com/java-applet)