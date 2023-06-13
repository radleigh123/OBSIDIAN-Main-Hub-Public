---
cssclass:
aliases:
tags:
- Java
- Java/Lecture
- Java/Thread
---
**[[Java|HOME [Java]]]**

---
>[!DONE|ttl-c]- Introduction
> In March of 2010 I was interviewed by Janice Heiss from Oracle (http://java.sun.com/developer/technicalArticles/Interviews/community/yakov_qa_2010.html), and she asked me to name the Java class I couldn’t live without. I didn’t think twice: Thread. This is where the power of Java resides. There are books devoted to Java threads, which give you amazing power and flexibility when it comes to building highly available, scalable, and responsive applications capable of processing thousands of concurrent requests of various types.
> 
> Up until now you’ve been creating Java programs that were executing code sequentially. But the main power of Java lies in its ability to do things in parallel, or, as they say, to run multiple threads of execution. As always, going through a practical use case is the best way to understand this feature.
> 
> Let’s discuss a program that should display market news and information about the user’s stock portfolio in the same window. While the market news feed is coming from a remote computer, stock portfolio data are retrieved from the database and may be located on the local machine.
> 
> Suppose it takes five seconds to get the market news and only three seconds to get the portfolio data. If you run these two tasks sequentially (one after another), you need eight seconds to complete the job.
> 
> But market news doesn’t depend on your portfolio data and these two tasks can run in parallel. They run on different computers and use different processors. If you can implement parallel processing, the total time should be less than eight seconds (close to five seconds in our use case — the time it takes for the longer task to complete).
> 
> A Java program can start multiple threads of execution that will run in parallel. Even if you have only one processor in your computer, it still could be a good idea to run some tasks in parallel. Think of a web browser that allows you to download a fi le and perform page browsing at the same time. Web browsers maintain two or more connections to any website, and can download multiple resources (text, images, videos, music) at the same time. Any web browser works in a multi-threaded mode.
> 
> If these jobs ran sequentially, the browser’s window would be frozen until the download was complete. On a multiprocessor computer, parallel threads can run on different CPUs. On a single-processor computer, threads will take turns getting “slices” of the processor’s time. Because switching CPU cycles between threads happens fast, a user won’t notice the tiny delays in each thread’s execution, and browsing will feel smooth.
> 
> In many cases, especially on single CPU computers, the benefit of many threads comes about because there’s a lot of idle time in most operations. In particular, if an operation is I/O bound instead of CPU bound using multiple threads helps take advantage of those otherwise unused blocks of time.
> 
> People also can work in a multi-threaded mode. For example, they can drink coffee while talking on a cell phone and driving a car. In the airport you can see people walking on the moving belt — they will reach their gate faster than by standing still.

# Multithreading
- process of executing multiple threads simultaneously
- helps maximum utilization of CPU
- they are independent, they don't affect the execution of other threads
- an exception in one thread will not interrupt other threads
- useful for serving multiple clients, multiplayer games, and other mutually independent tasks

example:
>[!aside|show-title right]+ RESULT:
> Thread #1: 10
> Thread #1: 9
> Thread #1: 8
> Thread #1: 7
> Thread #1: 6
> Thread #1: 5
> Thread #1: 4
> Thread #1: 3
> Thread #1: 2
> Thread #1: 1
> Thread#1 is finished
> Thread #2: 0
> Thread #2: 1
> Thread #2: 2
> Thread #2: 3
> Thread #2: 4
> Thread #2: 5
> Thread #2: 6
> Thread #2: 7
> Thread #2: 8
> Thread #2: 9

```java
public class Proto {
    public static void main(String[] args) {

        // creathing thread
        myThread thread1 = new myThread();

        // another alternative creating thread
        myRunnable runnable1 = new myRunnable();
        Thread thread2 = new Thread(runnable1);

        thread1.start();
        thread1.join(3000); // until thread1 dies, thread2 will play
        thread2.start();

    }
}
```
```java
/**
* myThread
*/

public class myThread extends Thread {

    @Override
    public void run() {
        for (int i = 10; i > 0; i--) {
            System.out.println("Thread #1: " + i);
            try {
                Thread.sleep(1000);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }

        System.out.println("Thread#1 is finished");
    }

}
```
```java
/**
* myRunnable
*/

public class myRunnable implements Runnable {

    @Override
    public void run() {
        for (int i = 0; i < 10; i++) {
            System.out.println("Thread #2: " + i);
            try {
                Thread.sleep(1000);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }

        System.out.println("Thread#2 is finished");
    }

}
```

<br>

# 
---
- https://www.simplilearn.com/tutorials/java-tutorial/multithreading-in-java
- https://www.tutorialspoint.com/java/java_multithreading.htm