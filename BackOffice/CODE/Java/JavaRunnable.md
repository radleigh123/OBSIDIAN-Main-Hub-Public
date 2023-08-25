---
cssclass:
title: JavaRunnable
creation-date: 2023-06-14
aliases:
tags:
- Java
- Java/Interface 
- Java/Runnable
---
**[[Java|HOME [Java]]]**

---
# `Runnable` Interface
The second way to create threads is to implement a `Runnable` interface. In this case your class also has to have business logic in the method run(). The second version of our market-portfolio example (source codes below) also has three classes, but `MarketNew2` and `Portfolio2` are not inherited from the class `Thread` — they implement the `Runnable` interface.

Creation of a thread in this case is a two-step process: create an instance of a class that implements `Runnable` and then give it as a constructor argument during instantiation of the class Thread.
```java
/**
 * MarketNews2.java
 */

public class MarketNews2 implements Runnable {
	public void run() {
		System.out.println("The stock market is improving!");
	}
}
```
```java
/**
 * Portfolio2.java
 */

public class Portfolio2 implements Runnable {
	public void run() {
		System.out.println("You have 500 shares of IBM");
	}
}
```
```java
/**
 * TestThreads2.java
 */

public class TestThreads2 {
	public static void main(String args[]){
		MarketNews2 mn2 = new MarketNews2();
		Thread mn = new Thread(mn2, "Market News");
		mn.start();
		
		Runnable port2 = new Portfolio2();
		Thread p = new Thread(port2, "Portfolio Data");
		p.start();
		System.out.println("TestThreads2 is finished");
	}
}
```
Note that I’ve declared the variable port2 in Listing 20-6 to be not of type `Portfolio2`, but of type `Runnable`. I did it for illustration purposes and to encourage you to use what you’ve learned about [[JavaInterface|casting to interfaces]]. It takes three lines of code in Listing 20-6 to instantiate and start a thread. You can do this in one line, but this syntax won’t give you a reference to the thread object should you need to call any methods on this object in the future (see variables `mn` and `p` above):
```java
(new Thread(new MarketNews2("Market News"))).start();
```
The `Runnable` interface provides a more flexible way to use threads, because it allows a class to be inherited from any other class, while having all the features of a thread. For example, a Swing [[Java#Java Applets (deprecated)|applet]] must be a subclass of a `javax.swing.JApplet`, and, because Java doesn’t support multiple inheritance, it should implement `Runnable` to support multithreading. 