---
aliases:
tags:
- Java
- Java/javax.swing.JButton
- Java/java.awt.event.ActionListener
- Java/java.awt.event.ActionEvent
- Java/JButton
- Java/AbstractButton
- Java/ActionListener
- Java/ActionEvent
---
**[[JavaSwing|BACK]]**

---
## JButtons
class is used to create a labeled button that has platform independent implementation. The application result in some action when the button is pushed. It inherits `AbstractButton` class.

**e.g.**
>[!aside|right show-title]+
> ![[JavaGUISwingJButtonimage0.png]]

```java
public class Proto {
    public static void main(String[] args) {
        new myFrame();
    }
}
```
```java
import javax.swing.JButton;
import javax.swing.JFrame;
import javax.swing.JPanel;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

public class myFrame extends JFrame {
    public myFrame() {
        // Create a panel to hold the button
        JPanel panel = new JPanel();

        // Create a button with the text "Click me"
        JButton button = new JButton("Click me");

        // Add an ActionListener to the button
        button.addActionListener(new ActionListener() {
            @Override
            public void actionPerformed(ActionEvent e) {
                System.out.println("Button clicked!");
            }
        });

        // Add the button to the panel
        panel.add(button);

        // Add the panel to the frame
        add(panel);

        // Set some frame properties
        setTitle("My Button Program");
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setSize(300, 200);
        setLocationRelativeTo(null); // center the frame on the screen
        setVisible(true);
    }
}
```
---
- **[[JavaGUISwingJButtonsample0|JButton w/ icons & using a lambda function]]**

<br>

# 
---
- https://docs.oracle.com/javase/7/docs/api/javax/swing/JButton.html
- [javatpoint/JButton](https://www.javatpoint.com/java-jbutton#:~:text=The%20JButton%20class%20is%20used,It%20inherits%20AbstractButton%20class.)