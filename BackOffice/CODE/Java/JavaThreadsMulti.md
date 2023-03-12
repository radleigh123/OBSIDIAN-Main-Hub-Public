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
## Multithreading
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