---
aliases:
tags:
- Java
- Java/javax.swing
- Java/javax.swing.event
- Java/JSlider
- Java/GUI/Swing/ChangeListener
---
**[[JavaGUISwingJSlider|BACK]]**

---
## Using a `ChangeListener`
>[!aside|show-title right]+ Result:
> ![[JavaGUISwingJSlidersampleimage.png|cover ws-med]]

```java
public class Proto {

    public static void main(String[] args) {
        new SliderDemo();
    }
}
```
```java
import java.awt.*;
import javax.swing.*;
import javax.swing.event.*;

public class SliderDemo implements ChangeListener {

    JFrame frame;
    JPanel panel;
    JLabel label;
    JSlider slider;

    SliderDemo() {

        frame = new JFrame("My Slider Demo");
        panel = new JPanel();
        label = new JLabel();
        slider = new JSlider(0, 100, 50);

        slider.setPreferredSize(new Dimension(400, 200));
        slider.setOrientation(SwingConstants.VERTICAL); // Change slider orientation
        slider.addChangeListener(this); // trigger ChangeListener

        slider.setPaintTicks(true);
        slider.setMinorTickSpacing(10);

        slider.setPaintTrack(true);
        slider.setMajorTickSpacing(25);

        slider.setPaintLabels(true);
        slider.setFont(new Font("Minecraft", Font.ITALIC, 15));

        label.setFont(new Font("Minecraft", Font.BOLD, 19));

        panel.add(slider);
        panel.add(label);
        frame.add(panel);
        frame.setSize(420, 400);
        frame.setVisible(true);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

    }

    @Override
    public void stateChanged(ChangeEvent e) {
        label.setText("°C = " + slider.getValue());
    }

}
```