---
aliases:
tags:
- Java
- Java/javax.swing
- Java/MouseListener
- Java/MouseEvent
- Java/java.awt
- Java/java.awt.event
- Java/setLocationRelativeTo
---
**[[Java|HOME [Java]]]**

---
## `MouseListener`
> The listener interface for receiving "interesting" mouse events (press, release, click, enter, and exit) on a component. (To track mouse moves and mouse drags, use the **[[JavaMouseMotionListener|MouseMotionListener]]**.

The Java **MouseListener** is notified whenever you change the state of mouse. It is notified against `MouseEvent`. The signature of 5 methods found in **MouseListener** interface are given below:
```java
public abstract void mouseClicked(MouseEvent e);

public abstract void mouseEntered(MouseEvent e);

public abstract void mouseExited(MouseEvent e);

public abstract void mousePressed(MouseEvent e);

public abstract void mouseReleased(MouseEvent e);

```

**e.g.**
>[!aside|show-title right]+ Result:
> ![[JavaMouseListenerimage.png|wsmall cover]]

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

public class myFrame extends JFrame implements MouseListener {

    JLabel label;

    myFrame() {

        label = new JLabel();
        label.setBounds(0, 0, 100, 100);
        label.setBackground(Color.RED);
        label.setOpaque(true);
        label.addMouseListener(this); // when label clicked, will execute code
        // this.addMouseListener(this); // entire frame will respond

        this.add(label);
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        this.setLayout(null);
        this.setSize(500, 500);
        this.setLocationRelativeTo(null); // set frame center on screen
        this.setVisible(true);

    }

    @Override
    public void mouseClicked(MouseEvent e) {
        // invoked when mouse button has been clicked (pressed & released) on component
        System.out.println("Mouse clicked...");
    }

    @Override
    public void mousePressed(MouseEvent e) {
        // invoked when a mouse button has been pressed on a component
        System.out.println("Mouse presssed...");
        label.setBackground(Color.YELLOW);
    }

    @Override
    public void mouseReleased(MouseEvent e) {
        // invoked when a mouse button has been released on a component
        System.out.println("Mouse released...");
        label.setBackground(Color.GREEN);
    }

    @Override
    public void mouseEntered(MouseEvent e) {
        // invoked when the mouse hovers in a component
        System.out.println("Mouse entered the component...");
        label.setBackground(Color.LIGHT_GRAY);
    }

    @Override
    public void mouseExited(MouseEvent e) {
        // invoked when the mouse hovers out a component
        System.out.println("Mouse exited the component...");
        label.setBackground(Color.GRAY);
    }
}
```

<br>

# 
---
- [MouseListener (Java Platform SE 7)](https://docs.oracle.com/javase/7/docs/api/java/awt/event/MouseListener.html)
	- **[How to write a Mouse Listener](https://docs.oracle.com/javase/tutorial/uiswing/events/mouselistener.html)**
- https://www.javatpoint.com/java-mouselistener