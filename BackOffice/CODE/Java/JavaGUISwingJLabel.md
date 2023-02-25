---
aliases:
tags:
- Java
- Java/Lecture
- Java/javax.swing.JLabel
- Java/javax.swing.ImageIcon
- Java/javax.swing.JFrame
- Java/javax.swing.BorderFactory
- Java/javax.swing.border.Border
- Java/java.awt.Color
- Java/java.awt.Font
- Java/ImageIcon
- Java/JFrame
- Java/JLabel
---
**[[JavaGUISwing|BACK]]**

---
## `JLabel`
is a class of java Swing.
- used to display a short string or an image icon;
- can display text, image or both and;
- only a display of text or image and it cannot get focus .

**e.g.**
>[!aside|right show-title]+ **Result:**
> ![[JavaGUISwingJLabelimage0.png|ws-med]]

```java
import java.awt.Color;
import java.awt.Font;

import javax.swing.BorderFactory;
import javax.swing.ImageIcon;
import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.border.Border;

public class Proto {
    public static void main(String[] args) {
        ImageIcon image = new ImageIcon("google.png");

        Border border = BorderFactory.createLineBorder(Color.green, 3);

        JLabel label = new JLabel(); // can put string literal, similar to `setTExt()`
        label.setText("Hello World");
        label.setIcon(image); // set image to label
        label.setHorizontalTextPosition(JLabel.CENTER);
        label.setVerticalTextPosition(JLabel.TOP);
        label.setForeground(new Color(0x00FF00)); // set font color
        label.setFont(new Font("Times New Roman", Font.BOLD, 35)); // set font of text
        label.setIconTextGap(-25); // set gap of text to image

        label.setOpaque(true); // display background color
        label.setBackground(Color.black);
        label.setBorder(border);
        label.setVerticalAlignment(JLabel.CENTER); // set vertical position of icon + text
        label.setHorizontalAlignment(JLabel.CENTER); // set horizontal position of icon + text
        // label.setBounds(100, 100, 350, 350); // set (x, y) position within frame

        JFrame frame = new JFrame();
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        // frame.setSize(420, 420);
        // frame.setLayout(null);
        frame.setVisible(true);
        frame.add(label);
        frame.setIconImage(image.getImage());
        frame.pack();
    }
}
```

<br>

# 
---
- https://docs.oracle.com/javase/7/docs/api/javax/swing/JLabel.html
- https://www.geeksforgeeks.org/jlabel-java-swing/