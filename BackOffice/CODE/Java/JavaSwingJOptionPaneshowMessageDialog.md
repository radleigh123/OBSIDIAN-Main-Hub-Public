---
aliases:
tags:
- Java
- Java/Lecture
- Java/javax.swing
- Java/JOptionPane/showMessageDialog
---
**[[JavaSwingJOptionPane|BACK]]**

---
## `showMessageDialog`
- shows input
- **parameter:** (`Component, Object, String, int, Icon`)
	- `Component` - determines which [[JavaGUISwingJFrame|Frame]] the dialog is displayed
	- `Object` - any objects e.g., "You have an error"
	- `String` - title of dialog
	- `int` - different **[[JavaMessageTypes|MessageTypes]]**
	- `Icon` - overrides the default *MessageType* icon


**Simple example**
```java
import javax.swing.JOptionPane;

public class Main {
    public static void main(String[] args) {
        String name = JOptionPane.showInputDialog("Enter your name");
		
        JOptionPane.showMessageDialog(null,
                "Hello " + name,
                "Inane error",
                JOptionPane.ERROR_MESSAGE);
    }
}
```

>[!INFO|clean no-i]- **Complex example**
>>[!aside|show-title right]+ Result:
>> ![[JavaGUISwingJOptionPaneshowMessageDialogimage0.png|ws-med cover]]
>
> ```java
> import javax.swing.*;
> import java.awt.Color;
> 
> public class Proto extends JFrame {
> 
>     public Proto() {
>         getContentPane().setBackground(Color.DARK_GRAY);
>         setTitle("Message Dialog in Frame");
>         setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
>         setVisible(true);
>         setResizable(false);
>         setSize(400, 300);
>         getContentPane().setLayout(null);
>     }
> 
>     public static void main(String[] args) {
>         ImageIcon icon = new ImageIcon("google.png");
>         JOptionPane.showMessageDialog(new Proto(),
>                 "I appear as part of the frame!!", "Customized Dialog",
>                 JOptionPane.INFORMATION_MESSAGE, icon);
>     }
> }
> ```

<br>

# 
---
- https://mkyong.com/swing/java-swing-how-to-make-a-simple-dialog/