---
aliases:
tags:
- Java
- Java/javax.swing
- Java/JFileChooser
- Java/java.awt
- Java/ActionListener
- Java/ActionEvent
---
**[[JavaGUISwingJFileChooser|BACK]]**

---
>[!aside|show-title right txt-c]+ Result:
> ![[JavaGUISwingJFileChoosersampleimage.png|cover ws-med]]
> ![[JavaGUISwingJFileChoosersampleimage1.png|cover ws-med]]

```java
public class Proto {
    public static void main(String[] args) {
        new myFrame();
    }
}
```
```java
import java.io.*;

import javax.swing.*;

import java.awt.*;
import java.awt.event.*;

public class myFrame extends JFrame implements ActionListener {

    JButton button;

    myFrame() {

        button = new JButton("Select a file");
        button.addActionListener(this);

        this.add(button);
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        this.setLayout(new FlowLayout());
        this.pack();
        this.setVisible(true);

    }

    @Override
    public void actionPerformed(ActionEvent e) {
        if (e.getSource() == button) {

            JFileChooser filechooser = new JFileChooser();
            filechooser.setCurrentDirectory(new File(".")); // `"."` set to current file location

            int respo = filechooser.showOpenDialog(null); // select a file to open
            // int respo = filechooser.showSaveDialog(null); // saves a file

            if (respo == JFileChooser.APPROVE_OPTION) {

                File file = new File(filechooser.getSelectedFile().getAbsolutePath());
                System.out.println(file);

            }

        }
    }

}

```