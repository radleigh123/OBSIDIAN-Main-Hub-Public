---
aliases:
tags:
- Java
- Java/javax.swing
- Java/JOptionPane/showConfirmDialog
---
**[[JavaSwingJOptionPane|BACK]]**

---
## `showConfirmDialog`
- get user input by asking a confirming question
- **parameters:** (`Component, Object, String, int, int, Icon`)
	- `Component` - determines which [[JavaGUISwingJFrame|Frame]] the dialog is displayed
	- `Object` - any objects e.g., "You have an error"
	- `String` - title of dialog
	- `int` - different **[[JavaOptionTypes|OptionTypes]]**
	- `int` - different **[[JavaMessageTypes|MessageTypes]]**
	- `Icon` - overrides the default *MessageType* icon

**Simple example**
```java
import javax.swing.*;

public class ConfirmDialog1 {
    public static void main(String[] args) {
        int input = JOptionPane.showConfirmDialog(null, "Do you like bacon?");
        // 0 = YES
        // 1 = NO
        // 2 = CANCEL
        
        System.out.println(input);
    }
}
```

**Complex example**
>[!aside|show-title right]+ Result:
> ![[JavaGUISwingJOptionPaneshowConfirmDialogimage0.png|wsmall cover]]

```java
import javax.swing.*;
import java.awt.Color;

public class Proto extends JFrame {

    public Proto() {
        getContentPane().setBackground(Color.DARK_GRAY);
        setTitle("Confirm Dialog in Frame");
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setVisible(true);
        setResizable(false);
        setSize(400, 300);
        getContentPane().setLayout(null);
    }

    public static void main(String[] args) {
        ImageIcon icon = new ImageIcon("src/images/turtle64.png");
        int input = JOptionPane.showConfirmDialog(
                new Proto(), // Component
                "I appear as part of the frame!!", // Object
                "Customized Dialog", // String
                JOptionPane.OK_CANCEL_OPTION, // int
                JOptionPane.INFORMATION_MESSAGE, // int
                icon); // Icon

        // 0=ok, 2=cancel
        System.out.println(input);
    }
}
```

<br>

# 
---
- https://mkyong.com/swing/java-swing-how-to-make-a-confirmation-dialog/