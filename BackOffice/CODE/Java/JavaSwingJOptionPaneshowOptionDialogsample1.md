---
aliases:
tags:
- Java
- Java/Lecture
- Java/java.awt
- Java/javax.swing
- Java/JOptionPane/showOptionDialog
- Java/JLabel
- Java/ImageIcon
- Java/JPanel
- Java/SupressWarnings
---
**[[JavaSwingJOptionPaneshowOptionDialog|BACK]]**

---
## Using with [[JavaSwingJOptionPaneshowConfirmDialog|showConfirmDialog]] and [[JavaGUISwingJFrame|JFrame]]
>[!aside|show-title right]
> ![[JavaGUISwingJOptionPaneshowOptionDialogsample1image0.png|cover wsmall]]
> 
> ![[JavaGUISwingJOptionPaneshowOptionDialogsample1image1.png|cover wsmall]]

```java
import javax.swing.*;
import java.awt.*;

@SuppressWarnings("serials")
public class Proto extends JFrame {
    public Proto() {
        this.getContentPane().setBackground(Color.LIGHT_GRAY);
        this.getContentPane().setLayout(null);
        this.setTitle("Confirm Dialog in Frame");
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        this.setVisible(true);
        this.setResizable(false);
        this.setSize(450, 300);

        Dimension dim = Toolkit.getDefaultToolkit().getScreenSize();
        setLocation(
                dim.width / 2 - this.getWidth() / 2,
                dim.height / 2 - this.getHeight() / 2);
    }

    public JPanel panel() {
        JPanel panel = new JPanel();
        panel.setBounds(0, 0, 444, 271);
        panel.setBackground(Color.CYAN);
        getContentPane().add(panel);
        panel.setLayout(null);

        JLabel lblIcon = new JLabel("");
        lblIcon.setBounds(30, 30, 200, 200);
        lblIcon.setIcon(new ImageIcon("google.png"));
        panel.add(lblIcon);

        JLabel lblText2 = new JLabel("Congratulations");
        lblText2.setVerticalAlignment(SwingConstants.TOP);
        lblText2.setFont(new Font("Tahoma", Font.BOLD, 14));
        lblText2.setHorizontalAlignment(SwingConstants.CENTER);
        lblText2.setBounds(240, 30, 175, 100);
        panel.add(lblText2);

        JLabel lblText1 = new JLabel("Ulol");
        lblText1.setHorizontalAlignment(SwingConstants.CENTER);
        lblText1.setFont(new Font("Times New Roman", Font.ITALIC, 14));
        lblText1.setBounds(240, 30, 175, 100);
        panel.add(lblText1);

        return panel;

    }

    public static void main(String[] args) {

        Proto proto = new Proto();
        ImageIcon icon = new ImageIcon("google.png");
        String[] op = { "Rhiz", "Caballero", "Anna", "Marie" };
        int num = JOptionPane.showOptionDialog(
                proto,
                "Abra kadabra",
                "Betlog",
                JOptionPane.DEFAULT_OPTION,
                JOptionPane.PLAIN_MESSAGE,
                icon,
                op,
                op[0]);

        if (num == 3) {
            proto.getContentPane().add(proto.panel());
            proto.repaint();
            proto.revalidate();
        } else {
            proto.dispose();
            JOptionPane.showMessageDialog(null, "Ehh wrong");
        }

    }

}
```