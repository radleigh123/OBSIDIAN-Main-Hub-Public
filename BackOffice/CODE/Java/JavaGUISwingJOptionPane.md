---
aliases:
tags:
- Java
- Java/Lecture
- Java/GUI/Swing/JOptionPane
- Java/javax.swing/JOptionPane
---
**[[JavaGUISwing|BACK]]**

---
## `JOptionPane`
makes it easy to pop up a standard dialog box that prompts users for a value or informs them of something.

**JOptionPane.showInputDialog()** - takes input
**JOptionPane.showMessageDialog()** - shows input
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

**Examples**
- [[JavaGUISwingJOptionPanesample0|Using `parseInt()` to output integer value]]
- [[JavaGUISwingJOptionPanesample1|Using `parseDouble()` to output floating-point value]]

<br>

# 
---
- **How to make Dialogs** - https://docs.oracle.com/javase/tutorial/uiswing/components/dialog.html
- https://docs.oracle.com/javase/7/docs/api/javax/swing/JOptionPane.html