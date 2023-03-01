---
title: JavaKeyListener
creation-date: 2023-02-28
aliases:
tags:
- Java
- Java/Lecture
- Java/java.awt
- Java/java.awt.event
- Java/KeyListener
- Java/KeyEvent
---
**[[JavaGUISwing|BACK]]**

---
# `KeyListener`
> The listener interface for receiving keyboard events (keystrokes)

The Java `KeyListener` is notified whenever you change the state of key. It is notified against `KeyEvent`.

**e.g.**
>[!aside|show-title right]+ Result:
> ![[JavaKeyListenerimage.png|cover wsmall]]

```java
public class Proto {
    public static void main(String[] args) {
        new myFrame();
    }
}
```
```java
import java.awt.*;
import java.awt.event.*;

import javax.swing.*;

public class myFrame extends JFrame implements KeyListener {

    JLabel label;

    myFrame() {

        label = new JLabel();
        label.setBounds(0, 0, 100, 100);
        label.setBackground(Color.BLACK);
        label.setOpaque(true);

        this.add(label);
        this.addKeyListener(this);
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        this.setLayout(null);
        this.setSize(500, 500);
        this.setVisible(true);

    }

    @Override
    public void keyTyped(KeyEvent e) {
        // keyTyped - invoked when a key is typed.
        // Uses KeyChar, char output
        switch (e.getKeyChar()) {
            case 'a':
                label.setLocation(label.getX() - 10, label.getY());
                break;
            case 'w':
                label.setLocation(label.getX(), label.getY() - 10);
                break;
            case 's':
                label.setLocation(label.getX(), label.getY() + 10);
                break;
            case 'd':
                label.setLocation(label.getX() + 10, label.getY());
                break;
        }
    }

    @Override
    public void keyPressed(KeyEvent e) {
        // keyPressed - invoked when a physical key is pressed down.
        // Uses KeyCode, int ouput
        switch (e.getKeyCode()) {
            case 37:
                label.setLocation(label.getX() - 10, label.getY());
                break;
            case 38:
                label.setLocation(label.getX(), label.getY() - 10);
                break;
            case 40:
                label.setLocation(label.getX(), label.getY() + 10);
                break;
            case 39:
                label.setLocation(label.getX() + 10, label.getY());
                break;
        }
    }

    @Override
    public void keyReleased(KeyEvent e) {
        // keyReleased - called whenever a button is released
        System.out.print("Key released: " + e.getKeyChar());
        System.out.println("\tKey code released: " + e.getKeyCode());
    }

}
```

<br>

# 
---
- [KeyListener (Java Platform SE 7)](https://docs.oracle.com/javase/7/docs/api/java/awt/event/KeyListener.html)
- https://www.javatpoint.com/java-keylistener