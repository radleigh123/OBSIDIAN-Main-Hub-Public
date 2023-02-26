---
aliases:
tags:
- Java
- Java/Lecture
- Java/javax.swing
- Java/JCheckBox
---
**[[JavaGUISwingJCheckBox|BACK]]**

---
## Using `JCheckBox` with `ActionListener`
>[!aside|show-title right]+ Result:
> ![[JavaGUISwingJCheckBoxsampleimage.png|cover ws-med]]

```java
public class Proto {
    public static void main(String[] args) {
        new myFrame();
    }
}
```
```java
import java.awt.event.ActionListener;
import java.awt.event.ActionEvent;
import java.awt.*;

import javax.swing.*;

public class myFrame extends JFrame implements ActionListener {

    JButton button;
    JCheckBox check;
    ImageIcon XIcon;
    ImageIcon CIcon;

    myFrame() {

        XIcon = new ImageIcon("google.png");
        CIcon = new ImageIcon("google.png");

        button = new JButton("Submit");
        button.addActionListener(this);

        check = new JCheckBox();
        check.setText("Venus Flytrap");
        check.setFocusable(false);
        check.setFont(new Font("Times New Roman", Font.BOLD, 35));
        check.setIcon(XIcon);
        check.setSelectedIcon(CIcon);

        this.add(button);
        this.add(check);
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        this.setLayout(new FlowLayout());
        this.pack();
        this.setVisible(true);

    }

    @Override
    public void actionPerformed(ActionEvent e) {
        if (e.getSource() == button) {
            System.out.println(check.isSelected());
        }
    }

}
```