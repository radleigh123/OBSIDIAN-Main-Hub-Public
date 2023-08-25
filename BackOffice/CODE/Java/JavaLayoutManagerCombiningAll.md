---
cssclass:
aliases:
tags:
- Java
- Java/javax.swing
- Java/java.awt
- Java/GridLayout
- Java/BorderLayout
- Java/JButton
- Java/JPanel
- Java/JTextField
- Java/JFrame
---
**[[Java#Introduction Graphical User Interface (GUI)|HOME [Java]]]**

---
## Combining Layout Managers
>[!aside|show-title right]+ RESULT:
> ![[JavaLayoutManagerCombiningAll.png|center]]

```java
/**
 * Main.java
 */
public class Main {
    public static void main(String[] args) {
        new Calc();
    }
}
```
```java
/**
 * Calc.java
 */
import javax.swing.*;

import java.awt.GridLayout;
import java.awt.BorderLayout;

public class Calc extends JFrame {

    // Declaring calculator components
    JPanel windowContent;
    JPanel p1;

    JTextField displayField;

    JButton button0;
    JButton button1;
    JButton button2;
    JButton button3;
    JButton button4;
    JButton button5;
    JButton button6;
    JButton button7;
    JButton button8;
    JButton button9;
    JButton buttonPoint;
    JButton buttonEqual;

    /*
     * Constructor creates the components and adds to the frame
     * using combination of BorderLayout and GridLayout
     */
    Calc() {

        windowContent = new JPanel();
        windowContent.setLayout(new BorderLayout()); // Layout Manager for this panel

        displayField = new JTextField();
        windowContent.add("North", displayField);

        // Creating buttons
        button0 = new JButton("0");
        button1 = new JButton("1");
        button2 = new JButton("2");
        button3 = new JButton("3");
        button4 = new JButton("4");
        button5 = new JButton("5");
        button6 = new JButton("6");
        button7 = new JButton("7");
        button8 = new JButton("8");
        button9 = new JButton("9");
        buttonPoint = new JButton(".");
        buttonEqual = new JButton("=");

        // Panel with 12 buttons - 10 numeric ones, period, and equal sign
        p1 = new JPanel();
        p1.setLayout(new GridLayout(4, 3)); // (rows, columns)

        // Adding window controls to panel
        p1.add(button1);
        p1.add(button2);
        p1.add(button3);
        p1.add(button4);
        p1.add(button5);
        p1.add(button6);
        p1.add(button7);
        p1.add(button8);
        p1.add(button9);
        p1.add(button0);
        p1.add(buttonPoint);
        p1.add(buttonEqual);

        windowContent.add("Center", p1); // add panel p1 to the center

        // Frame and its Content Pane
        this.setTitle("Calculator");
        this.setContentPane(windowContent);
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        this.pack(); // size of window big enough to accomodate all controls
        this.setVisible(true);
        this.setLocationRelativeTo(null);

    }

}
```