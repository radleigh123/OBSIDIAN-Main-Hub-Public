---
aliases:
tags:
- Java
- Java/Lecture
- Java/javax.swing
- Java/JSlider
---
**[[JavaSwing|BACK]]**

---
## `JSlider` class
A component that lets the user graphically select a value by sliding a knob within a bounded interval

![[JavaGUISwingJSliderimage.png|center cover hs-med]]

**e.g.**
>[!aside|show-title right]+ Result:
> ![[JavaGUISwingJSliderimage1.png]]

```java
import javax.swing.*;

public class Proto extends JFrame {

    public Proto() {

        JSlider slider = new JSlider(JSlider.VERTICAL, 0, 50, 25);
        JPanel panel = new JPanel();

        panel.add(slider);
        this.add(panel);

    }

    public static void main(String[] args) {
        Proto proto = new Proto();

        proto.pack();
        proto.setVisible(true);
        proto.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        proto.setLayout(null);
    }
}
```

More example:
- [[JavaGUISwingJSlidersample|Using a ChangeListener]]

<br>

# 
---
- [JSlider (Java Platform SE 7)](https://docs.oracle.com/javase/7/docs/api/javax/swing/JSlider.html)
	- **[how to use Sliders](https://docs.oracle.com/javase/tutorial/uiswing/components/slider.html)**
- https://www.javatpoint.com/java-jslider