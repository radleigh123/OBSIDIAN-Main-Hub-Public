---
aliases:
tags:
- Java
- Java/java.awt
- Java/javax.swing
- Java/JLayeredPane
- Java/JFrame
- Java/JLabel
---
**[[JavaSwing|BACK]]**

---
## `LayeredPane` class
is used to add depth to swing container. It is used to provide a third dimension for positioning component and divide the depth-range into several different layers.
![[JavaGUISwingJLayeredPaneimage0.png|wsmall center]]

>[!FAQ|txt-c ttl-c] **JLayeredPane** class declaration
> ```java
> public class JLayeredPane extends JComponent implements Accessible
> ```

**e.g.**
>[!aside|show-title right]+ Result:
> ![[JavaGUISwingJLayeredPaneimage1.png|cover ws-med]]

```java
import java.awt.Color;

import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.JLayeredPane;

public class Proto {
    public static void main(String[] args) {

        JLabel label1 = new JLabel("Hello World");
        label1.setOpaque(true);
        label1.setBackground(Color.LIGHT_GRAY);
        label1.setBounds(50, 50, 200, 200);

        JLabel label2 = new JLabel("Hello Mars");
        label2.setOpaque(true);
        label2.setBackground(Color.RED);
        label2.setBounds(100, 100, 200, 200);

        JLabel label3 = new JLabel("Hello Venus");
        label3.setOpaque(true);
        label3.setBackground(Color.CYAN);
        label3.setBounds(150, 150, 200, 200);

        JLayeredPane layered = new JLayeredPane();
        layered.setBounds(0, 0, 500, 500);
        layered.add(label1, JLayeredPane.DEFAULT_LAYER); // Ordering panes
        layered.add(label2, JLayeredPane.DEFAULT_LAYER); // DEFAULT_LAYER == Integer.valueOf(0)
        layered.add(label3, JLayeredPane.DRAG_LAYER); // DEFAULT_LAYER == Integer.valueOf(5)

        JFrame frame = new JFrame();
        frame.add(layered);

        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setSize(600, 500);
        frame.setLayout(null);
        frame.setVisible(true);
    }
}
```

<br>

# 
---
- [JLayeredPane (Java Platform SE 7)](https://docs.oracle.com/javase/7/docs/api/javax/swing/JLayeredPane.html)
	- [**How to use JLayeredPane**](https://docs.oracle.com/javase/tutorial/uiswing/components/layeredpane.html)
- https://www.javatpoint.com/java-jlayeredpane