---
aliases:
tags:
- Java
- Java/Lecture
- Java/javax.swing
- Java/JTextField
---
**[[JavaGUISwingJTextField|BACK]]**

---
## Storing the text field input
>[!aside|show-title right]+ Result:
> ![[JavaGUISwingJTextFieldsampleimage.png|cover]]

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
    JTextField txtF;

    myFrame() {

        button = new JButton("enter");
        button.addActionListener(this);

        txtF = new JTextField();
        txtF.setPreferredSize(new Dimension(250, 40));
        txtF.setFont(new Font("Consolas", Font.TRUETYPE_FONT, 35));
        txtF.setForeground(Color.LIGHT_GRAY);
        txtF.setBackground(Color.BLACK);
        txtF.setCaretColor(Color.WHITE);
        txtF.setText("username");
        // txtF.setEditable(false); // enable/disable edit text field

        this.add(button);
        this.add(txtF);
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        this.setLayout(new FlowLayout());
        this.pack();
        this.setVisible(true);

    }

    @Override
    public void actionPerformed(ActionEvent e) {
        if (e.getSource() == button) {
            System.out.println("Welcome " + txtF.getText());
            button.setEnabled(false);
            txtF.setEditable(false);
        }
    }

}
```