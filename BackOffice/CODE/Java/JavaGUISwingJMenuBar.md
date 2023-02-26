---
aliases:
tags:
- Java
- Java/javax.swing
- Java/JMenuBar
- Java/JMenu
- Java/JMenuItem
---
**[[JavaGUISwing|BACK]]**

---
## `JMenuBar`, `JMenu`, `JMenuItem` class
> An implementation of a menu bar. You add `JMenu` objects to the menu bar to construct a menu

The object of `JMenu` class is a pull down menu component which is displayed from the menu bar. It inherits the **`JMenuItem`** class.

**e.g.**
>[!aside|show-title right]+ Result:
> ![[JavaGUISwingJMenuBarimage.png|ws-med cover]]

```java
import javax.swing.*;

public class Proto2 extends JFrame {

    JMenu menu, subMenu;
    JMenuItem i1, i2, i3, i4, i5;

    Proto2() {

        JFrame frame = new JFrame("Menu demo");
        JMenuBar mBar = new JMenuBar();

        menu = new JMenu("Menu");
        subMenu = new JMenu("Sub-Menu");
        i1 = new JMenuItem("Item 1");
        i2 = new JMenuItem("Item 2");
        i3 = new JMenuItem("Item 3");
        i4 = new JMenuItem("Item 4");
        i5 = new JMenuItem("Item 5");

        menu.add(i1);
        menu.add(i2);
        menu.add(i3);
        subMenu.add(i4);
        subMenu.add(i5);
        menu.add(subMenu);
        mBar.add(menu);

        frame.setJMenuBar(mBar);
        frame.setSize(400, 200);
        frame.setLayout(null);
        frame.setVisible(true);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

    }

    public static void main(String[] args) {
        new Proto2();
    }

}
```

More examples:
- [[JavaGUISwingJMenuBarsample|Using a `ActionListener`]]

<br>

# 
---
- [JMenuBar (Java Platform SE 7)](https://docs.oracle.com/javase/7/docs/api/javax/swing/JMenuBar.html)
- [JMenuBar (Java Platform SE 8)](https://docs.oracle.com/javase/8/docs/api/javax/swing/JMenuBar.html)
- https://www.javatpoint.com/java-jmenuitem-and-jmenu