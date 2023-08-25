---
aliases:
tags:
- Java
- Java/JColorChooser
---
**[[JavaSwing|BACK]]**

---
## `JColorChooser` class
> provides a pane of controls designed to allow a user to manipulate and select a color

The `JColorChooser` class is used to create a color chooser dialog box so that user can select any color. It inherits [[JavaJComponent|JComponent]] class.

**e.g. with <u>ActionListener</u>**
>[!aside|show-title right]+ Result:
> ![[JavaGUISwingJColorChooserimage.png]]
> ![[JavaGUISwingJColorChooserimage1.png]]

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

public class myFrame extends JFrame implements ActionListener {

    JButton button;
    JLabel label;

    myFrame() {

        button = new JButton("Pick a color");
        button.addActionListener(this);

        label = new JLabel();
        label.setBackground(Color.WHITE);
        label.setOpaque(true);
        label.setText("This is some text");
        label.setFont(new Font("Times New Roman", Font.ITALIC, 100));

        this.add(button);
        this.add(label);
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        this.setLayout(new FlowLayout());
        this.pack();
        this.setVisible(true);

    }

    @Override
    public void actionPerformed(ActionEvent e) {
        if (e.getSource() == button) {

            JColorChooser colorchooser = new JColorChooser();

            Color color = JColorChooser.showDialog(null, "Pick a color", Color.RED);

            // label.setForeground(color);
            label.setBackground(color);

        }
    }

}
```

<br>

# 
---
- [JColorChooser (Java Platform SE 7)](https://docs.oracle.com/javase/7/docs/api/javax/swing/JColorChooser.html)
	- **[How to use color choosers](https://docs.oracle.com/javase/tutorial/uiswing/components/colorchooser.html)**
- https://www.javatpoint.com/java-jcolorchooser