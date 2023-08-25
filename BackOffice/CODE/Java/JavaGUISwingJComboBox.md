---
aliases:
tags:
- Java
- Java/javax.swing
- Java/JComboBox
---
**[[JavaSwing|BACK]]**

---
## `JComboBox` class
> A component that combines a button or editable field and a drop-down list

The object of Choice class is used to show popup menu of choices. Choice selected by user is shown on the top of a menu. It inherits [[JavaJComponent|JComponent]] class.

**e.g.**
>[!aside|show-title right]+ Result:
> ![[JavaGUISwingJComboBoximage.png|cover ws-med]]

```java
import javax.swing.*;

public class Proto {
    public static void main(String[] args) {
        JFrame frame = new JFrame("ComboBox sample");

        String[] nation = { "Asia", "Africa", "America", "Arctic" };

        JComboBox<String> cb = new JComboBox<String>(nation);

        cb.setBounds(50, 50, 90, 20);
        frame.add(cb);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setLayout(null);
        frame.setSize(400, 500);
        frame.setVisible(true);

    }
}
```

More examples:
- [[JavaGUISwingJComboBoxsample|Using with ActionListener]]

<br>

# 
---
- [JComboBox (Java Platform SE 7)](https://docs.oracle.com/javase/7/docs/api/javax/swing/JComboBox.html)
	- **[How to Use Combo Boxes](https://docs.oracle.com/javase/tutorial/uiswing/components/combobox.html)**
- https://www.javatpoint.com/java-jcombobox