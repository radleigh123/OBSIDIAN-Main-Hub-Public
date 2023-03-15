---
aliases:
tags:
- Java
- Java/GUI/Swing/JOptionPane
- Java/javax.swing/JOptionPane
- Java/WrapperClass/Integer/parseInt
---
**[[JavaSwingJOptionPane|BACK]]**

---
## Using `parseInt()` to output integer value
a method in the `Integer` class that is used to parse a string representation of an integer into an **int** value.

**e.g.**
```java
import javax.swing.JOptionPane;

public class Main {
    public static void main(String[] args) {
        int age = Integer.parseInt(JOptionPane.showInputDialog("Enter your age:"));
        JOptionPane.showMessageDialog(
                null,
                "You are " + age,
                "User's age",
                JOptionPane.INFORMATION_MESSAGE);
    }
}
```

<br>

# 
---
- https://www.tutorialspoint.com/java/number_parseint.htm