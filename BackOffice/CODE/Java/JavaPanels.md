---
aliases:
tags:
- Java
- Java/Lecture
- Java/javax.swing.JPanel
- Java/JPanel
---
**[[JavaGUISwing|BACK]]**

---
## `JPanel`
is a container that can store a group of components. The main task of `JPanel` is to organize components, various layouts can be set in `JPanel` which provide better organization of components, however, it does not have a title bar.

**e.g.**
>[!aside|right show-title]+ **Result:**
> ![[JavaPanelsimage0.png|ws-small]]

```java
import java.awt.Color;

import javax.swing.ImageIcon;
import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.JPanel;

public class Proto {
    public static void main(String[] args) {
        ImageIcon icon = new ImageIcon("google.png");

        JLabel label = new JLabel();
        label.setText("Hello");
        label.setIcon(icon);

        JPanel blueP = new JPanel();
        blueP.setBackground(Color.RED);
        blueP.setBounds(0, 0, 250, 250);

        JPanel redP = new JPanel();
        redP.setBackground(Color.BLUE);
        redP.setBounds(250, 0, 250, 250);

        JPanel greenP = new JPanel();
        greenP.setBackground(Color.GREEN);
        greenP.setBounds(0, 250, 500, 250);

        JFrame frame = new JFrame();
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setVisible(true);
        frame.setLayout(null);
        frame.setSize(600, 600);

        redP.add(label);
        blueP.add(label);
        frame.add(blueP);
        frame.add(redP);
        frame.add(greenP);
    }
}
```

<br>

# 
---
- https://docs.oracle.com/javase/7/docs/api/javax/swing/JPanel.html
- https://www.geeksforgeeks.org/java-swing-jpanel-with-examples/