---
aliases:
tags:
- Java
- Java/Lecture
- Java/java.awt
- Java/FlowLayout
- Java/javax.swing
- Java/JFrame
---
**[[JavaSwing|BACK]]**

---
## `FlowLayout` class
is a layout manager in Java that arranges components in a single row, adding new components to the right of the previous one.
**e.g.**
>[!aside|show-title right]+ Result:
> ![[JavaLayoutManagerFlowimage0.png|cover ws-med]]

```java
import javax.swing.*;
import java.awt.*;

public class Proto extends JFrame {
    public Proto() {
        setTitle("FlowLayout Example");
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setSize(400, 300);

        // Create a new FlowLayout for the JFrame
        FlowLayout flowLayout = new FlowLayout();
        setLayout(flowLayout); // Set the layout of the JFrame to the FlowLayout

        JButton button1 = new JButton("Button 1");
        add(button1);
        JButton button2 = new JButton("Button 2");
        add(button2);
        JButton button3 = new JButton("Button 3");
        add(button3);

        setVisible(true);
    }

    public static void main(String[] args) {
        new Proto();
    }
}
```

<br>

**e.g.**
>[!aside|show-title right]+ Result:
> ![[JavaLayoutManagerFlowimage1.png|cover ws-med]]

```java
import java.awt.*;
import java.awt.FlowLayout;

import javax.swing.*;

public class Proto {
    public static void main(String[] args) {

        JFrame frame = new JFrame();
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setSize(500, 500);
        frame.setLayout(new FlowLayout(FlowLayout.CENTER, 5, 10));

        JPanel panel = new JPanel();
        panel.setPreferredSize(new Dimension(100, 250));
        panel.setBackground(Color.LIGHT_GRAY);
        panel.setLayout(new FlowLayout());

        // direct instantiate Jbutton
        panel.add(new JButton("1"));
        panel.add(new JButton("2"));
        panel.add(new JButton("3"));
        panel.add(new JButton("4"));
        panel.add(new JButton("5"));
        panel.add(new JButton("6"));
        panel.add(new JButton("7"));
        panel.add(new JButton("8"));
        panel.add(new JButton("9"));

        frame.add(panel);
        frame.setVisible(true);
    }
}
```

<br>

# 
---
- [FlowLayout (Java Platform SE 7)](https://docs.oracle.com/javase/7/docs/api/java/awt/FlowLayout.html#:~:text=public%20class%20FlowLayout%20extends%20Object,ComponentOrientation.)
	- [**How to use FlowLayout**](https://docs.oracle.com/javase/tutorial/uiswing/layout/flow.html)
- https://www.javatpoint.com/FlowLayout