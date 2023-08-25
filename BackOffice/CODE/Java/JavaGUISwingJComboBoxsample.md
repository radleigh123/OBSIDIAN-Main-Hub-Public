---
aliases:
tags:
- Java
- Java/JComboBox
---
**[[JavaGUISwingJComboBox|BACK]]**

---
## Using with `ActionListener`
>[!aside|show-title right]+ Result:
> ![[Pasted image 20230225174023.png|cover ws-med]]

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

    JComboBox<String> cBox;

    myFrame() {

        String[] animals = { "dog", "cat", "bird" };
        // use wrapper class like Integer, Double because of primitive data types

        cBox = new JComboBox<>(animals);
        cBox.addActionListener(this);

        // cBox.setEditable(true); // set to type
        // System.out.println(cBox.getItemCount());
        // cBox.addItem("horse");
        cBox.insertItemAt("pig", 0);
        // cBox.setSelectedIndex(0);
        // cBox.removeItem("cat");
        // cBox.removeItemAt(0);
        // cBox.removeAllItems();

        this.add(cBox);
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        this.setLayout(new FlowLayout());
        this.pack();
        this.setVisible(true);

    }

    @Override
    public void actionPerformed(ActionEvent e) {
        if (e.getSource() == cBox) {
            System.out.println(cBox.getSelectedItem());
            // System.out.println(cBox.getSelectedIndex());
        }
    }

}
```