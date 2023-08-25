---
aliases:
tags:
- Java
- Java/javax.swing
- Java/JCheckBox
- Java/JFrame
- Java/JButton
---
**[[JavaSwing|BACK]]**

---
## `JCheckBox` class
> an item that can be selected or deselected, and which displays its state to the user

It is used to turn an option on (true) or off (false). Clicking on a CheckBox changes its state from "on" to "off" or from "off" to "on". It inherits [[JavaJToggleButton|JToggleButton]] class.

**e.g.**
>[!aside|show-title right]+ Result:
> ![[JavaGUISwingJCheckBoximage.png|cover wsmall]]

```java
import javax.swing.*;

public class CheckBoxExample {

     CheckBoxExample() {
        JFrame f= new JFrame("CheckBox Example");
          
        JCheckBox checkBox1 = new JCheckBox("C++");  
        checkBox1.setBounds(100,100, 50,50);
          
        JCheckBox checkBox2 = new JCheckBox("Java", true);  
        checkBox2.setBounds(100,150, 50,50);
          
        f.add(checkBox1);  
        f.add(checkBox2);  
        f.setSize(400,400);  
        f.setLayout(null);  
        f.setVisible(true);
    }  
	
	public static void main(String args[]) {  
	    new CheckBoxExample();
	}
	
}  
```

More examples
- [[JavaGUISwingJCheckBoxsample|Using JCheckBox with ActionListener]]

<br>

# 
---
- [JCheckBox (Java Platforms SE 7)](https://docs.oracle.com/javase/7/docs/api/javax/swing/JCheckBox.html)
	- [**How to use Buttons, Check Boxes, and Radio Buttons**](https://docs.oracle.com/javase/tutorial/uiswing/components/button.html)
- https://www.javatpoint.com/java-jcheckbox#:~:text=The%20JCheckBox%20class%20is%20used,It%20inherits%20JToggleButton%20class.