---
cssclass:
title: JavaEventListeners
creation-date: 2023-03-17
aliases:
tags:
- Java
- Java/java.awt
- Java/java.awt.event
- Java/ActionListener
---
**[[UpdateJava#Event Handling in UI|HOME [Java]]]**

---
# Event Listeners
$\quad$Swing widgets can process various events, or in the programmers’ jargon can "*listen to events*". To listen to events, a program has to register window components with Java classes called **listeners**.

$\quad$To process button clicks Swing provides **ActionListener**. All listeners are declared as Java [[JavaInterface|interfaces]] and their [[JavaMethod|methods]] have to be implemented in an object that will be listening to events. This is how Java documentation describes the ActionListener interface:
> $\quad$The listener interface for receiving action events. The class that is interested in processing an action event implements this interface, and the object created with that class is registered with a component, using the component’s `addActionListener` method. When the action event occurs, that object’s `actionPerformed` method is invoked.

The interface is defined in the `java.awt.event` [[JavaPackages|package]]. The `actionPerformed` method is invoked by the [[JavaJDK&JRE|JVM]] if the action happened.
```java
public interface ActionListener extends EventListener {
	void actionPerformed(ActionEvent e);
}
```

<br>

# 
---
- [Introduction to Event Listeners (Oracle)](https://docs.oracle.com/javase/tutorial/uiswing/events/intro.html)
- [Java Event Handling (javaTpoint)](https://www.javatpoint.com/event-handling-in-java)