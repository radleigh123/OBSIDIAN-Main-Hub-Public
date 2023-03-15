---
aliases:
tags:
- Java
- Java/Lecture
- Java/javax.swing
- Java/java.awt
- Java/JFrame
- Java/JFrame/dispose
- Java/JLabel
- Java/ActionListener
---
**[[JavaSwing|BACK]]**

---
## Launching another window
**main**
```java
public class Proto {
    public static void main(String[] args) {
        launchPage launchpage = new launchPage();
    }
}
```
**launchPage**
```java
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

import javax.swing.JButton;
import javax.swing.JFrame;

public class launchPage implements ActionListener {
    JFrame frame = new JFrame();
    JButton button = new JButton("Hello World");

    launchPage() {

        button.setBounds(100, 160, 200, 40);
        button.setFocusable(false);
        button.addActionListener(this);
        frame.add(button);

        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setSize(420, 420);
        frame.setLayout(null);
        frame.setVisible(true);

    }

    @Override
    public void actionPerformed(ActionEvent e) {
        if (e.getSource() == button) {

            frame.dispose();
            newWindow window = new newWindow();

        }
    }
}
```
**newWindow**
```java
import java.awt.Font;

import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.plaf.FontUIResource;

public class newWindow {

    JFrame frame = new JFrame();
    JLabel label = new JLabel("Hello");

    newWindow() {

        label.setBounds(0, 0, 100, 50);
        label.setFont(new FontUIResource("Times New Roman", Font.BOLD, 25));

        frame.add(label);

        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setSize(420, 420);
        frame.setLayout(null);
        frame.setVisible(true);

    }
}
```