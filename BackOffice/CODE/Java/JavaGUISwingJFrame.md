---
aliases:
tags:
- Java
- Java/Lecture
- Java/javax.swing.JFrame
- Java/JFrame/setVisible
- Java/JFrame/setSize
- Java/JFrame/setTitle
- Java/JFrame/setDefaultCloseOperation
- Java/JFrame/setResizable
- Java/JFrame/setIconImage
- Java/JFrame/getContentPane
- Java/javax.swing.ImageIcon
- Java/ImageIcon/getImage
- Java/java.awt.Color
- Java/Color/setBackground
---
**[[JavaSwing|BACK]]**

---
## `JFrame`
> a GUI window to add components to

The `javax.swing.JFrame` class is a type of container which inherits the `java.awt.Frame` class. **JFrame** works like the main window where components like labels, buttons, textfields are added to create a GUI.

<center>Two ways creating a <strong>Frame</strong>:</center>

**Creating an instance of JFrame:**
>[!aside|right show-title]+ **Result**
> ![[JavaGUISwingJFrameimage0.png|center cover ws-med]]

```java
import java.awt.Color;
import javax.swing.ImageIcon;
import javax.swing.JFrame;

public class Proto {
    public static void main(String[] args) {
        JFrame frame = new JFrame();
        frame.setTitle("Pornhub");
        frame.setResizable(false); // prevent frame resizing

        frame.setVisible(true); // set frame visible
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE); // default(HIDE_ON_CLOSE), DO_NOTHING_ON_CLOSE
        frame.setSize(420, 420); // sets the x and y of frame

        // --------------------------------------------

        ImageIcon image = new ImageIcon("google.png");
        frame.setIconImage(image.getImage()); // change icon of frame

        // --------------------------------------------

        frame.getContentPane().setBackground(Color.yellow); // change color of background
        frame.getContentPane().setBackground(new Color(255, 255, 255)); // custom color or can use HEX no.
    }
}
```

**JFrame as a parent class**
>[!aside|right show-title]+ **Result**
> Same as the shown image above

```java
/**
* Main file
*/
public class Proto {
    public static void main(String[] args) {
	    myFrame myframe = new myFrame();
        new myFrame(); // direct call of constructor
    }
}
```

```java
/**
* myFrame class
*/
import java.awt.Color;

import javax.swing.ImageIcon;
import javax.swing.JFrame;

public class myFrame extends JFrame {
    myFrame() {
        this.setTitle("Pornhub");
        this.setResizable(false); // prevent frame resizing

        this.setVisible(true); // set frame visible
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE); // default(HIDE_ON_CLOSE), DO_NOTHING_ON_CLOSE
        this.setSize(420, 420); // sets the x and y of frame

        // --------------------------------------------

        ImageIcon image = new ImageIcon("google.png");
        this.setIconImage(image.getImage()); // change icon of frame

        // --------------------------------------------

        this.getContentPane().setBackground(Color.yellow); // change color of background
        this.getContentPane().setBackground(new Color(255, 255, 255)); // custom color or can use HEX no.
    }
}
```

<br>

# 
---
- https://www.javatpoint.com/java-jframe
- https://docs.oracle.com/javase/7/docs/api/javax/swing/JFrame.html