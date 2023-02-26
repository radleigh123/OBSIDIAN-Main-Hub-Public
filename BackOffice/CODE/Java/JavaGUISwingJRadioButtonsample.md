---
aliases:
tags:
- Java
- Java/javax.swing
- Java/JRadioButton
---
**[[JavaGUISwingJRadioButton|BACK]]**

---
## Using with `ActionListener`
>[!aside|show-title right]+ Result:
> ![[JavaGUISwingJRadioButtonsampleimage.png|cover wsmall]]

```java
public class Proto {
    public static void main(String[] args) {
        new myFrame();
    }
}
```
```java
import java.awt.event.*;
import java.awt.*;

import javax.swing.*;

public class myFrame extends JFrame implements ActionListener {

    JRadioButton rButton1, rButton2, rButton3;
    ImageIcon XIcon, CIcon;

    myFrame() {

        XIcon = new ImageIcon("play.png");
        CIcon = new ImageIcon("play1.png");

        rButton1 = new JRadioButton("pizza");
        rButton2 = new JRadioButton("hamburger");
        rButton3 = new JRadioButton("hotdog");

        rButton1.setFocusable(false);
        rButton2.setFocusable(false);
        rButton3.setFocusable(false);

        rButton1.addActionListener(this);
        rButton2.addActionListener(this);
        rButton3.addActionListener(this);

        rButton1.setIcon(XIcon);
        rButton2.setIcon(XIcon);
        rButton3.setIcon(XIcon);

        rButton1.setSelectedIcon(CIcon);
        rButton2.setSelectedIcon(CIcon);
        rButton3.setSelectedIcon(CIcon);

        ButtonGroup group = new ButtonGroup();
        group.add(rButton1);
        group.add(rButton2);
        group.add(rButton3);

        this.add(rButton1);
        this.add(rButton2);
        this.add(rButton3);
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        this.setLayout(new FlowLayout());
        this.pack();
        this.setVisible(true);

    }

    @Override
    public void actionPerformed(ActionEvent e) {
        if (e.getSource() == rButton1) {
            System.out.println("Button1 clicked...");
        } else if (e.getSource() == rButton2) {
            System.out.println("Button2 clicked...");
        } else if (e.getSource() == rButton3) {
            System.out.println("Button3 clicked...");
        }
    }

}
```