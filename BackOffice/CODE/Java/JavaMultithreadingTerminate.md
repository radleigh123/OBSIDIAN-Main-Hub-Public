---
cssclass:
aliases:
tags:
- Java
- Java/Multithreading
- Java/Thread
---
**[[Java|HOME [Java]]]**

---
**Creating an object implementing the `Runnable` interface**
>[!aside|right]-
> StoppableRunnable running
> ...
> ...
> ...
> ...
> requesting stop
> stop requested
> ...
> StoppableRunnable stopped

```java
package Multithreading.Stopping.unit1;

public class StoppableRunnable implements Runnable {
    private boolean stopRequested = false;

    public synchronized void requestStop() {
        this.stopRequested = true;
    }

    public synchronized boolean isStopRequested() {
        return this.stopRequested;
    }

    private void sleep(long millis) {
        try {
            Thread.sleep(millis);
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
    }

    @Override
    public void run() {
        System.out.println("StoppableRunnable running");
        while (!isStopRequested()) {
            sleep(1000);
            System.out.println("...");
        }
        System.out.println("StoppableRunnable stopped");
    }
}
```
```java
package Multithreading.Stopping.unit1;

public class ThreadExample {
    public static void main(String[] args) {
        StoppableRunnable stoppableRunnable = new StoppableRunnable();
        Thread thread = new Thread(stoppableRunnable, "The Thread");
        thread.start();

        try {
            Thread.sleep(5000);
        } catch (InterruptedException e) {
            e.printStackTrace();
        }

        System.out.println("requesting stop");
        stoppableRunnable.requestStop();
        System.out.println("stop requested");
    }
}
```

**Using a Daemon method `setDaemon()`**
>[!aside|right]-
> Running
> Running
> Running
> Running
> Running
> Running

```java
package Multithreading.Stopping.unit2;

public class ThreadExample {
    public static void main(String[] args) {
        Runnable runnable = () -> {
            while (true) {
                sleep(500);
                System.out.println("Running");
            }
        };

        Thread thread = new Thread(runnable);
        thread.setDaemon(true);
        thread.start();
        sleep(3100);
    }

    public static void sleep(long millis) {
        try {
            Thread.sleep(millis);
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
    }
}
```