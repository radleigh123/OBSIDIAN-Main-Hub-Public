---
aliases:
tags:
- Java
- Java/Lecture
- Java/javax.swing
- Java/JProgressBar
---
**[[JavaGUISwing|BACK]]**

---
## `JProgressBar` class
> A component that visually displays the progress of some task

The `JProgressBar` class is used to display the progress of the task. It inherits **[[JavaJComponent|JComponent]]** class.

![[JavaGUISwingJProgressBarimage.png|cover hs-med center]]

**e.g.**
>[!aside|show-title right]+ Result:
> ![[JavaGUISwingJProgressBarimage1.png]]

```java
import javax.swing.*;

public class Proto2 extends JFrame {

    JProgressBar progress;
    int i = 0, num = 0;

    Proto2() {

        this.setVisible(true);

        progress = new JProgressBar(0, 100);
        progress.setBounds(40, 40, 160, 30);
        progress.setValue(50);
        progress.setStringPainted(true);

        this.add(progress);
        this.setSize(250, 150);
        this.setLayout(null);
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

    }

    public static void main(String[] args) {
        new Proto2();
    }

}
```

More examples:
- [[JavaGUISwingJProgressBarsample|Using a Thread.sleep() method]]

<br>

# 
---
- [JProgressBar (Java Platform SE 7)](https://docs.oracle.com/javase/7/docs/api/javax/swing/JProgressBar.html)
	- **[How to use Progress Bars](https://docs.oracle.com/javase/tutorial/uiswing/components/progress.html)**
- https://www.javatpoint.com/java-jprogressbar