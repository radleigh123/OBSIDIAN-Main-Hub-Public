---
cssclass:
title: JavaThread
creation-date: 2023-06-14
aliases:
tags:
- Java
- 
---
**[[UpdateJava|HOME [Java]]]**

---
## The Class Thread
If class `A` needs to initiate some executions in classes `B` and `C`, the latter two must declare multi-threading support from the get-go. Each of the classes `B` and `C` must either be inherited from the Java class Thread or implement one of the following interfaces: Runnable or Callable (the latter is covered in Lesson 21). If a class is inherited from the class Thread it has to override the method run().

The first version of the market-portfolio example has three classes (see Listings 20-1, -2, and -3). Two of them are subclasses of the class Thread (`MarketNews` and `Portfolio`), and the third (`TestThreads`) is just a testing program that instantiates them and starts the execution of some code in each of them. You must initiate the code that has to work as a thread in the method `run()`.
>[!WARNING|ttl-c] WARNING
> The suggested method is by implementing the `Runnable` interface, see [[JavaRunnable|next chapter]].

```java
/**
 * MarketNews.java
 * DEPRECATED
 */

public class MarketNews extends Thread {
	public MarketNews (String threadName) {
		super(threadName); // name your thread
	}
	
	public void run() {
		System.out.println("The stock market is improving!");
	}
}
```
```java
/**
 * Portfolio.java
 * DEPRECATED
 */

public class Portfolio extends Thread {
	public Portfolio (String threadName) {
		super(threadName);
	}
	
	public void run() {
		System.out.println("You have 500 shares of IBM");
	}
}
```
```java
/**
 * TestThreads.java
 */

public class TestThreads {
	public static void main(String args[]){
		MarketNews mn = new MarketNews("Market News");
		mn.start();
		
		Portfolio p = new Portfolio("Portfolio data");
		p.start();
		System.out.println("TestThreads is finished");
	}
}
```
The method `main()` above instantiates each thread, passing the name for the thread as a constructor argument, and then calls its `start()` method. Each thread itself invokes internally the code located in its method `run()`. After calling `mn.start()`, the program `TestThread` does not wait for its completion but immediately executes the lines that follow, creating and starting the thread Portfolio. Even if `MarketNews` will take time, the `Portfolio` thread will start immediately.

If you run the `TestThread` program it’ll print the output from threads `MarketNews` and `Portfolio` almost simultaneously — there is no lengthy and time-consuming code in their `run()` methods. A bit later, in the section [[JavaMultithreadingSleeping|Sleeping Threads,]] it'll show you how to emulate a lengthy execution. The output of the `TestThread` program can vary — it all depends on which thread will finish first.