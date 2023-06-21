---
cssclass:
aliases:
tags:
- Java
- Java/Thread
- Java/Multithreading
---
**[[UpdateJava|HOME [Java]]]**

---
**Creating a `Thread` object**
>[!aside|right]-
> Successfully ended thread

```java
package Multithreading.Initializing.unit1;

public class ThreadExample {
    public static void main(String[] args) {
        Thread thread = new Thread();
        thread.start();

        System.out.println("Successfully ended thread");
    }
}
```

**Inheriting the `Thread` class** (<mark class="hltr-lightred">DEPRECATED</mark>)
```java
package Multithreading.Initializing.unit2;

public class MyThread extends Thread {
    public void run() {
        System.out.println("MyThread running");
        System.out.println("MyThread finished");
    }
}
```
```java
package Multithreading.Initializing.unit2;

public class ThreadExample {
    public static void main(String[] args) {
        MyThread myThread = new MyThread();
        myThread.start();
    }
}
```

**Implementing the `Runnable` interface**
>[!aside|right]-
> MyRunnable::run::Thread started
> MyRunnable::run::Thread finished

```java
package Multithreading.Initializing.unit3;

public class MyRunnable implements Runnable {
    @Override
    public void run() {
        System.out.println("MyRunnable::run::Thread started");
        System.out.println("MyRunnable::run::Thread finished");
    }
}
```
```java
package Multithreading.Initializing.unit3;

public class ThreadExample {
    public static void main(String[] args) {
        Thread thread = new Thread(new MyRunnable());
        thread.start();
    }
}
```

**An anonymous class implementing the `Runnable` interface**
>[!aside|right]-
> Runnable running
> Runnable finished

```java
package Multithreading.Initializing.unit4;

public class ThreadExample {
    public static void main(String[] args) {
        Runnable runnable = new Runnable() {
            @Override
            public void run() {
                System.out.println("Runnable running");
                System.out.println("Runnable finished");
            }
        };

        Thread thread = new Thread(runnable);
        thread.start();
    }
}
```

**Using a Lambda expression**
```java
package Multithreading.Initializing.unit5;

public class ThreadExample {
    public static void main(String[] args) {
        Runnable runnable = () -> {
            System.out.println("Lambda Runnable running");
            System.out.println("Lambda Runnable finished");
        };

        Thread thread = new Thread(runnable);
        thread.start();
    }
}
```

**Passing a String literal**
>[!aside|right]-
> Processing...
> The Thread running

```java
package Multithreading.Initializing.unit5;

public class ThreadExample2 {
    public static void main(String[] args) {
        Runnable runnable = () -> {
            String threadName = Thread.currentThread().getName();
            System.out.println(threadName + " running");
        };

        try {
            System.out.println("Processing...");
            Thread.sleep(2000);
        } catch (InterruptedException e) {
            e.printStackTrace();
        }

        Thread thread = new Thread(runnable, "The Thread");
        thread.start();
    }
}
```