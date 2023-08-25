---
aliases:
tags:
- Java
- Java/javax.swing
- Java/JRadioButton
---
**[[JavaSwing|BACK]]**

---
## `JRadioButton` class
is used to create a radio button. It is used to choose one option from multiple options. It is widely used in exam systems or quiz.

>[!WARNING|alt-co] It should be added in [[JavaButtonGroup|`ButtonGroup`]] to select one radio button only

**e.g.**
>[!aside|show-title right]+ Result:
> ![[JavaJRadioButtonimage.png|center wsmall]]

```java
import javax.swing.*;

public class RadioButtonExample {

	JFrame f;
	
	RadioButtonExample(){
		f=new JFrame();
		JRadioButton r1=new JRadioButton("A) Male");
		JRadioButton r2=new JRadioButton("B) Female");
		r1.setBounds(75,50,100,30);
		r2.setBounds(75,100,100,30);
		ButtonGroup bg=new ButtonGroup();
		bg.add(r1);bg.add(r2);
		f.add(r1);f.add(r2);
		f.setSize(300,300);
		f.setLayout(null);
		f.setVisible(true);
	}
	public static void main(String[] args) {
	    new RadioButtonExample();
	}
	
}
```

More examples:
- [[JavaGUISwingJRadioButtonsample|Using with ActionListener]]

<br>

# 
---
- [JRadioButton (Java Platform SE 7)](https://docs.oracle.com/javase/7/docs/api/javax/swing/JRadioButton.html)
	- [**How to Use Buttons, Check Boxes, and Radio Buttons**](https://docs.oracle.com/javase/tutorial/uiswing/components/button.html)
- https://www.javatpoint.com/java-jradiobutton