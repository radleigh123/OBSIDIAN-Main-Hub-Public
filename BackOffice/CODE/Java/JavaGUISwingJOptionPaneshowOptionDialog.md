---
aliases:
tags:
- Java
- Java/Lecture
- Java/javax.swing
- Java/JOptionPane/showOptionDialog
---
**[[JavaGUISwingJOptionPane|BACK]]**

---
## `showOptionDialog`
- the Grand Unification of [[JavaGUISwingJOptionPaneshowConfirmDialog|showConfirmDialog]], [[JavaGUISwingJOptionPaneshowInputDialog|showInputDialog]] and [[JavaGUISwingJOptionPaneshowMessageDialog|showMessageDialog]]
- returns an `integer` which represents the position of the user’s choice in the `Object[]`

<br>

**Simple example**
>[!aside|show-title right]+ Result:
> ![[JavaGUISwingJOptionPaneshowOptionDialogimage0.png|cover wsmall]]

```java
import javax.swing.*;

public class Proto {
    public static void main(String[] args) {

        String[] options = new String[] { "op1", "op2", "op3", "op4" };

        int num = JOptionPane.showOptionDialog(
                null,
                "Returns the position of choice",
                "Click a button",
                JOptionPane.DEFAULT_OPTION,
                JOptionPane.INFORMATION_MESSAGE,
                null,
                options,
                options[0]);

        System.out.println(num);

    }
}
```

**Complex examples:**
- [[JavaGUISwingJOptionPaneshowOptionDialogsample0|Using array as an `Object[]`]]
- [[JavaGUISwingJOptionPaneshowOptionDialogsample1|Using with showConfirmDialog and JFrame]]

<br>

# 
---
- [JOptionPane (Java Platform SE 7)](https://docs.oracle.com/javase/7/docs/api/javax/swing/JOptionPane.html)
	- [**How to Make Dialogs**](https://docs.oracle.com/javase/tutorial/uiswing/components/dialog.html)
- https://mkyong.com/swing/java-swing-joptionpane-showoptiondialog-example/