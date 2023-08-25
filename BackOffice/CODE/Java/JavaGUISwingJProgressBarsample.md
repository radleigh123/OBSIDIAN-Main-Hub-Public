---
aliases:
tags:
- Java
- Java/javax.swing
- Java/java.awt
- Java/JProgressBar
- Java/Thread/sleep()
- Java/Exceptions/try
- Java/Exceptions/catch
- Java/Exceptions/InterruptedException
---
**[[JavaGUISwingJProgressBar|BACK]]**

---
## Using a `Thread.sleep()` method
>[!aside|show-title right]+ Result:
> ![[JavaGUISwingJProgressBarsampleimage.png|cover ws-med]]

```java
public class Proto {
    public static void main(String[] args) {
        new demo();
    }
}
```
```java
import java.awt.*;
import javax.swing.*;

public class demo {

    JFrame frame = new JFrame();
    JProgressBar bar = new JProgressBar(0, 100);

    demo() {

        bar.setValue(0);
        bar.setBounds(0, 0, 250, 50);
        bar.setStringPainted(true); // adds a percentage to bar
        bar.setForeground(Color.RED);
        bar.setBackground(Color.BLACK);

        frame.add(bar);
        frame.setSize(300, 150);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setLayout(null);
        frame.setVisible(true);

        fill();

    }

    public void fill() {

        int count = 0;

        while (count <= 100) {

            bar.setValue(count);
            
            try { Thread.sleep(50); }
            catch (InterruptedException e) { e.printStackTrace(); }
            
            count += 1;
        }

        bar.setString("Done!");
        bar.setFont(new Font("Minecraft", Font.BOLD, 25));

    }

}
```

<br>

# 
---
- **Thread.sleep()** - https://www.javatpoint.com/thread-sleep-in-java