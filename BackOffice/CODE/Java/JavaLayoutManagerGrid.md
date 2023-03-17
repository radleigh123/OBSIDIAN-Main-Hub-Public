---
aliases:
tags:
- Java
- Java/Lecture
- Java/java.awt
- Java/GridLayout
- Java/javax.swing
- Java/JFrame
---
**[[JavaSwing|BACK]]**

---
## `GridLayout` class
> places components in a grid of cells

is used to arrange the components in a rectangular grid. One component is displayed in each rectangle.

**e.g.**
>[!aside|show-title right]+ Result:
> ![[JavaLayoutManagerGridimage0.png|show-title ws-med]]

```java
import javax.swing.*;
import java.awt.*;

public class Proto {

    public static void main(String[] args) {
        JFrame frame = new JFrame();
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setSize(600, 500);
        frame.setLayout(new GridLayout(3, 3, 5, 5));

        frame.add(new JButton("1"));
        frame.add(new JButton("2"));
        frame.add(new JButton("3"));
        frame.add(new JButton("4"));
        frame.add(new JButton("5"));
        frame.add(new JButton("6"));
        frame.add(new JButton("7"));
        frame.add(new JButton("8"));
        frame.add(new JButton("9"));
        frame.add(new JButton("10"));

        frame.setVisible(true);
    }
}
```

More examples:
$\;$▪$\,$[[JavaLayoutManagerGridSample|Complex GridLayout Demo]]

<br>

# 
---
- [GridLayout (Java Platform SE 7)](https://docs.oracle.com/javase/7/docs/api/java/awt/GridLayout.html#:~:text=The%20GridLayout%20class%20is%20a,is%20placed%20in%20each%20rectangle.)
	- [**How to use GridLayout**](https://docs.oracle.com/javase/tutorial/uiswing/layout/grid.html)
- https://www.javatpoint.com/GridLayout