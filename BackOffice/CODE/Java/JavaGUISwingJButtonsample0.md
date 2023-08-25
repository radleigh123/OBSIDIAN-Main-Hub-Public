---
aliases:
tags:
- Java
- Java/java.awt.event.ActionListener
- Java/java.awt.event.ActionEvent
- Java/java.awt.Image
- Java/javax.swing.ImageIcon
- Java/javax.swing.BorderFactory
- Java/JButton
- Java/AbstractButton
- Java/ActionListener
- Java/ActionEvent
- Java/Image
- Java/ImageIcon
- Java/BorderFactory/createEtchedBorder
- Java/Lambda
---
**[[JavaGUISwingJButton|BACK]]**

---
## `JButton` w/ icons & using a lambda function
>[!aside|right show-title]+
> ![[JavaButtonssample0image0.png|cover ws-med]]

```java
public class Proto {
	public static void main(String[] args) {
		new myFrame();
	}
}
```
```java
import java.awt.Color;
import java.awt.Font;
import java.awt.Image;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.BorderFactory;
import javax.swing.ImageIcon;
import javax.swing.JButton;

public class myFrame extends JFrame implements ActionListener {

    JButton button;
    JLabel label;

    myFrame() {

        ImageIcon icon = new ImageIcon("google.png");

        // creating a new Image object w/ desired size
        Image image = icon.getImage();
        Image newImage = image.getScaledInstance(50, 50, Image.SCALE_SMOOTH);
        icon = new ImageIcon(newImage);

        label = new JLabel();
        label.setIcon(icon);
        label.setBounds(150, 250, 150, 150);
        label.setVisible(false);

        button = new JButton("sampleButton");
        button.setBounds(100, 100, 250, 100);
        button.addActionListener(this);
        // button.addActionListener(e -> System.out.println("clicked")); // use of
        // lambda expressions
        button.setFocusable(false);
        button.setIcon(icon);
        button.setHorizontalTextPosition(JButton.CENTER);
        button.setVerticalTextPosition(JButton.BOTTOM);
        button.setFont(new Font("Comic Sans", Font.ITALIC, 25));
        button.setIconTextGap(-12);
        button.setForeground(Color.CYAN);
        button.setBackground(Color.LIGHT_GRAY);
        button.setBorder(BorderFactory.createEtchedBorder());
        button.setEnabled(true); // if false, button is unusable

        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        this.setLayout(null);
        this.setSize(500, 500);
        this.setVisible(true);
        this.add(button);
        this.add(label);
    }

    @Override
    public void actionPerformed(ActionEvent e) {
        if (e.getSource() == button) {
            // System.out.println("clicked");
            label.setVisible(true);
        }
    }
}
```