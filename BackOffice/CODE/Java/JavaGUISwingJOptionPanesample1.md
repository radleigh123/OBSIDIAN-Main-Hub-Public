---
aliases:
tags:
- Java
- Java/GUI/Swing/JOptionPane
- Java/javax.swing/JOptionPane
- Java/Double/parseDouble
---
**[[JavaGUISwingJOptionPane|BACK]]**

---
## Using `parseDouble()` to output floating-point value
method of Java `Double` class returns a new double value that is initialized to the value corresponding to defined String.
**e.g.**
```java
import javax.swing.JOptionPane;

public class Main {
    public static void main(String[] args) {
        double height = Double.parseDouble(JOptionPane.showInputDialog("Enter dick height:"));
        JOptionPane.showMessageDialog(
                null,
                height + " in inches",
                "User's height",
                JOptionPane.WARNING_MESSAGE);
    }
}
```

<br>

# 
---
- https://www.javatpoint.com/java-double-parsedouble-method