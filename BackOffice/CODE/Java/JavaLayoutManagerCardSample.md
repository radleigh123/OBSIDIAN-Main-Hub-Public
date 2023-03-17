---
cssclass:
aliases:
tags:
- Java
- Java/java.awt
- Java/CardLayout
---
**[[JavaLayoutManagerCard|BACK]]**

---
>[!aside|show-title right]+ RESULT:
> ![[JavaLayoutManagerCardSample.png|center wsmall]]

```java
import java.awt.CardLayout;
import java.awt.Color;
import java.awt.Dimension;
import javax.swing.JButton;
import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.JPanel;

public class Main {
    public static void main(String[] args) {
        // Create a new JFrame
        JFrame frame = new JFrame("CardLayout Demo");

        // Create a new JPanel with a CardLayout
        JPanel cardPanel = new JPanel(new CardLayout());

        // Add the first panel to the cardPanel
        JPanel panel1 = new JPanel();
        panel1.setBackground(Color.RED);
        panel1.setPreferredSize(new Dimension(200, 200));
        panel1.add(new JLabel("Panel 1"));
        cardPanel.add(panel1, "Panel 1");

        // Add the second panel to the cardPanel
        JPanel panel2 = new JPanel();
        panel2.setBackground(Color.BLUE);
        panel2.setPreferredSize(new Dimension(200, 200));
        panel2.add(new JLabel("Panel 2"));
        cardPanel.add(panel2, "Panel 2");

        // Show the first panel by default
        CardLayout cardLayout = (CardLayout) cardPanel.getLayout();
        cardLayout.show(cardPanel, "Panel 1");

        // Create a button to switch between panels
        JButton button = new JButton("Switch Panels");
        button.addActionListener(e -> {
            cardLayout.next(cardPanel);
        });

        // Add the cardPanel and button to the frame
        frame.add(cardPanel);
        frame.add(button, "South");

        // Set the frame properties and make it visible
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.pack();
        frame.setVisible(true);
        frame.setLocationRelativeTo(null);
    }
}
```