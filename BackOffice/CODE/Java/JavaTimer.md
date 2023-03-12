---
cssclass:
title: JavaTimer
creation-date: 2023-03-12
aliases:
tags:
- Java
- Java/java.util
- Java/Timer
- Java/TimerTask
---
**[[Java|HOME [Java]]]**

---
# `Timer` class
A facility for threads to schedule tasks for future execution in a background thread.

`TimerTask` - a task that can be scheduled for one-time or repeated execution by a *Timer*

>[!aside|show-title right]+ RESULT:
> 10 seconds
> 9 seconds
> 8 seconds
> 7 seconds
> 6 seconds
> 5 seconds
> 4 seconds
> 3 seconds
> 2 seconds
> 1 seconds
> Happy New Year

```java
import java.util.*;

public class Proto {
    public static void main(String[] args) {

        Timer timer = new Timer();

        TimerTask task = new TimerTask() {

            int counter = 10;

            @Override
            public void run() {
                if (counter > 0) {
                    System.out.println(counter + " seconds");
                    counter--;
                } else {
                    System.out.println("Happy New Year");
                    timer.cancel();
                }
            }

        };

        Calendar date = Calendar.getInstance();
        date.set(Calendar.YEAR, 2023);
        date.set(Calendar.MONTH, Calendar.MARCH);
        date.set(Calendar.DAY_OF_MONTH, 12);
        date.set(Calendar.HOUR_OF_DAY, 14);
        date.set(Calendar.MINUTE, 58);
        date.set(Calendar.SECOND, 0);
        date.set(Calendar.MILLISECOND, 0);

        // timer.schedule(task, date.getTime());
        // timer.scheduleAtFixedRate(task, 0, 1000);

        timer.scheduleAtFixedRate(task, date.getTime(), 1000);
    }
}
```

<br>

# 
---
- https://docs.oracle.com/javase/7/docs/api/java/util/Timer.html
- https://www.baeldung.com/java-timer-and-timertask