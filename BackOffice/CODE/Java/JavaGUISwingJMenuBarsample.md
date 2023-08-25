---
aliases:
tags:
- Java
- Java/javax.swing
- Java/JMenuBar
- Java/JMenu
- Java/JMenuItem
- Java/ActionListener
- Java/ActionEvent
---
**[[JavaGUISwingJMenuBar|BACK]]**

---
## Using a `ActionListener`
>[!aside|show-title right]+ Result:
> ![[Pasted image 20230226154110.png|cover ws-med]]

```java
public class Proto {
    public static void main(String[] args) {
        new demo();
    }
}
```
```java
import java.awt.*;
import java.awt.event.*;

import javax.swing.*;

public class demo extends JFrame implements ActionListener {

    JMenuBar mBar;
    JMenu editMenu, fileMenu, helpMenu;
    JMenuItem loadItem, saveItem, exitItem;
    ImageIcon icon = new ImageIcon("play.png");

    demo() {

        mBar = new JMenuBar();

        editMenu = new JMenu("Edit Menu");
        fileMenu = new JMenu("File Menu");
        helpMenu = new JMenu("Help Menu");

        loadItem = new JMenuItem("Load items");
        saveItem = new JMenuItem("Save item");
        exitItem = new JMenuItem("Exit item");

        loadItem.addActionListener(this);
        saveItem.addActionListener(this);
        exitItem.addActionListener(this);

        // Adding icons to menu items
        loadItem.setIcon(icon);
        saveItem.setIcon(icon);
        exitItem.setIcon(icon);

        // Adding icon to file menu
        fileMenu.setIcon(icon);

        // Menu shortcut keys
        fileMenu.setMnemonic(KeyEvent.VK_Q); // alt + q for file menu
        editMenu.setMnemonic(KeyEvent.VK_W); // alt + w for edit menu
        helpMenu.setMnemonic(KeyEvent.VK_E); // alt + e for help menu

        // Menu Item shortcut keys
        loadItem.setMnemonic(KeyEvent.VK_A); // a for load
        saveItem.setMnemonic(KeyEvent.VK_S); // s for save
        exitItem.setMnemonic(KeyEvent.VK_D); // d for exit

        fileMenu.add(loadItem);
        fileMenu.add(saveItem);
        fileMenu.add(exitItem);
        mBar.add(fileMenu);
        mBar.add(editMenu);
        mBar.add(helpMenu);

        this.setJMenuBar(mBar);

        this.setVisible(true);
        this.setSize(400, 200);
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        this.setLayout(new FlowLayout());
    }

    @Override
    public void actionPerformed(ActionEvent e) {

        if (e.getSource() == loadItem) {
            System.out.println("Loading item...");
        } else if (e.getSource() == saveItem) {
            System.out.println("Saving item...");
        } else if (e.getSource() == exitItem) {
            System.exit(0);
        }

    }

}
```