---
cssclass:
title: JavaThreads
creation-date: 2023-03-12
aliases:
tags:
- Java
- Java/Thread
---
**[[Java|HOME [Java]]]**

---
# `Thread` class
*Thread class* provide [[JavaConstructors|constructors]] and [[JavaMethod|methods]] to create and perform operations on a *thread*. It extends [[JavaObject|Object]] class and implements `Runnable interface`. There are two ways to create a thread:
1.  By extending Thread class
2.  By implementing Runnable interface.

example:
>[!aside|show-title right]+ RESULT:
> Name: YAMETE!!!
> Priority: 10
> isAlive: true
> 3
> 2
> 1
> You dones

```java
public class Proto {
    public static void main(String[] args) throws InterruptedException {

        Thread.currentThread().setName("YAMETE!!!");
        System.out.println("Name: " + Thread.currentThread().getName());

        Thread.currentThread().setPriority(10);
        System.out.println("\nPriority: " + Thread.currentThread().getPriority());

        System.out.println("isAlive: " + Thread.currentThread().isAlive());

        for (int i = 3; i > 0; i--) {
            System.out.println(i);
            Thread.sleep(1000);
        }

        System.out.println("You dones");

    }
}
```

<br>

# 
---
- https://docs.oracle.com/javase/7/docs/api/java/lang/Thread.html
- https://www.w3schools.com/java/java_threads.asp
- https://www.javatpoint.com/how-to-create-a-thread-in-java