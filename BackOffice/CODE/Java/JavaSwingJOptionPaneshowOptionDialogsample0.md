---
aliases:
tags:
- Java
- Java/JOptionPane/showOptionDialog
---
**[[JavaSwingJOptionPane|BACK]]**

---
## Using array as an `Object[]`
>[!aside|show-title right]+ Result:
> ![[JavaGUISwingJOptionPaneshowOptionDialogsample0image.png|cover wsmall]]

```java
import javax.swing.*;

public class Proto {
    public static void main(String[] args) {

        JCheckBox check = new JCheckBox("Lick me");
        Object[] op = { 'A', 250, 1.5, "Mars", check };

        int num = JOptionPane.showOptionDialog(
                null,
                "Many option!",
                "Tick me now",
                JOptionPane.DEFAULT_OPTION,
                JOptionPane.ERROR_MESSAGE,
                null,
                op,
                op[0]);

        if (check.isSelected() && num != -1) {
            System.out.println("Your choice was " + op[num]);
        } else {
            System.out.println("Zero choice");
        }

    }
}
```