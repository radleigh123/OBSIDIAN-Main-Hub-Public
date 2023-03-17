---
cssclass:
aliases:
tags:
- Java
- Java/GridBagLayout
- Java/GridBagConstraints
---
**[[JavaLayoutMangerGridBag|BACK]]**

---
>[!aside|show-title right]+ RESULT:
> ![[JavaLayoutMangerGridBagSample.png|center wsmall]]

```java
import java.awt.GridBagConstraints;
import java.awt.GridBagLayout;
import javax.swing.JButton;
import javax.swing.JFrame;
import javax.swing.JPanel;

public class Main {
    public static void main(String[] args) {
        // Create a new JFrame
        JFrame frame = new JFrame("GridBagLayout Demo");

        // Create a new JPanel with a GridBagLayout
        JPanel panel = new JPanel(new GridBagLayout());

        // Define the GridBagConstraints for the buttons
        GridBagConstraints gbc = new GridBagConstraints();
        gbc.gridwidth = GridBagConstraints.REMAINDER;
        gbc.fill = GridBagConstraints.HORIZONTAL;

        // Add some buttons to the panel with different cell sizes
        panel.add(new JButton("Button 1"), gbc);
        gbc.weightx = 1.0;
        panel.add(new JButton("Button 2"), gbc);
        gbc.weightx = 0.0;
        gbc.gridwidth = 1;
        panel.add(new JButton("Button 3"), gbc);
        panel.add(new JButton("Button 4"), gbc);

        // Add the panel to the frame and set the frame properties
        frame.add(panel);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setSize(300, 300);
        frame.setVisible(true);
        frame.setLocationRelativeTo(null);
    }
}
```