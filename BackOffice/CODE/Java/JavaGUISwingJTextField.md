---
aliases:
tags:
- Java
- Java/Lecture
- Java/javax.swing
- Java/JTextField
---
**[[JavaGUISwing|BACK]]**

---
## `JTextField` class
> is a lightweight component that allows the editing of a single line of text.

The object of a JTextField class is a text component that allows the editing of a single line text. It inherits [[JavaJTextComponent|JTextComponent]] class.

**e.g.**
>[!aside|show-title right]
> ![[JavaGUISwingJTextFieldimage.png|cover wsmall]]

```java
import javax.swing.*;

public class Proto {

    public static void main(String[] args) {

        JFrame frame = new JFrame("TextField Example");
        JTextField text1, text2;

        text1 = new JTextField("Text 1 yo");
        text1.setBounds(50, 100, 200, 30);

        text2 = new JTextField("Texty 2");
        text2.setBounds(50, 150, 200, 30);

        frame.add(text1);
        frame.add(text2);
        frame.setSize(400, 400);
        frame.setLayout(null);
        frame.setVisible(true);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

    }

}
```

More examples:
- [[JavaGUISwingJTextFieldsample|Storing the text field input]]


<br>

# 
---
- [JTextField (Java Platform SE 7)](https://docs.oracle.com/javase/7/docs/api/javax/swing/JTextField.html#:~:text=JTextField%20is%20a%20lightweight%20component,is%20reasonable%20to%20do%20so.)
	- [**How to use Text Fields**](https://docs.oracle.com/javase/tutorial/uiswing/components/textfield.html)
- https://www.javatpoint.com/java-jtextfield