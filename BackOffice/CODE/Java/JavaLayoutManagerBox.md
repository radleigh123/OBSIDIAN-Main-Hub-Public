---
aliases:
tags:
- Java
- Java/javax.swing
- Java/BoxLayout
---
**[[JavaSwing|BACK]]**

---
## `BoxLayout` class
puts components in a single row or column. It respects the components' requested maximum sizes and also lets you align components.

$\quad$Unlike with the [[JavaLayoutManagerFlow|FlowLayout]] manager, when the window with the *BoxLayout* is resized, its controls do not wrap. And unlike with [[JavaLayoutManagerGrid|GridLayout]] manager, with *BoxLayout*, window controls can have different sizes.

Example:
>[!aside|show-title right]+ RESULT:
> ![[JavaLayoutManagerBox.png|center wsmall]]

```java
import javax.swing.Box;
import javax.swing.BoxLayout;
import javax.swing.JButton;
import javax.swing.JFrame;
import javax.swing.JPanel;

public class Main {
    public static void main(String[] args) {
        // Create a new JFrame
        JFrame frame = new JFrame("BoxLayout Demo");

        // Create a new JPanel with a vertical BoxLayout
        JPanel panel = new JPanel();
        panel.setLayout(new BoxLayout(panel, BoxLayout.Y_AXIS));

        // Add some buttons to the panel
        panel.add(new JButton("Button 1"));
        panel.add(Box.createVerticalStrut(10));
        panel.add(new JButton("Button 2"));
        panel.add(Box.createVerticalStrut(10));
        panel.add(new JButton("Button 3"));
        panel.add(Box.createVerticalStrut(10));
        panel.add(new JButton("Button 4"));

        // Add the panel to the frame and set the frame properties
        frame.add(panel);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setSize(300, 300);
        frame.setVisible(true);
        frame.setLocationRelativeTo(null);
    }
}
```

<br>

# 
---
- [How to Use BoxLayout](https://docs.oracle.com/javase/tutorial/uiswing/layout/box.html)