---
cssclass:
aliases:
tags:
- Java
- Java/Lecture
- Java/javax.swing
- Java/java.awt
- Java/JFrame
- Java/ImageIcon/getImage
- Java/Graphics
---
**[[Java|HOME [Java]]]**

---
## 2D Graphics
>[!aside|show-title right]+ RESULT:
> ![[JavaSample2DGraphicsimage.png|center wsmall]]

```java
public class Proto {
    public static void main(String[] args) {
        new myFrame();
    }
}
```
```java
import javax.swing.*;

public class myFrame extends JFrame {

    myPanel panel;

    myFrame() {

        panel = new myPanel();

        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        this.add(panel);
        this.pack(); // fit
        this.setLocationRelativeTo(null); // appear in the middle screen
        this.setVisible(true);

    }

}
```
```java
import java.awt.*;
import javax.swing.*;

public class myPanel extends JPanel {

    Image image;

    myPanel() {
        image = new ImageIcon("play.png").getImage(); // create an image out of the ImageIcon
        this.setPreferredSize(new Dimension(500, 500));
    }

    public void paint(Graphics g) {

        Graphics2D g2D = (Graphics2D) g; // updated version of Graphics

        // Line
        g2D.drawLine(0, 0, 500, 500);

        // Rectangle
        g2D.setStroke(new BasicStroke(4));
        g2D.setPaint(Color.BLUE);
        g2D.drawRect(5, 5, 300, 100);

        g2D.setPaint(Color.PINK);
        g2D.fillRect(5, 5, 300, 100); // overlaps the recent rectangle

        // Circle/Oval
        g2D.setPaint(Color.ORANGE);
        g2D.fillOval(5, 110, 50, 50);
        g2D.setStroke(new BasicStroke(2));
        g2D.setPaint(Color.BLACK);
        g2D.drawOval(5, 110, 50, 50);

        // Arcs
        g2D.setPaint(Color.RED);
        g2D.drawArc(5, 150, 100, 100, 180, 180);

        // Polygon (Triangle, Hexagon, etc.)
        int[] xPoints = { 150, 250, 350 };
        int[] yPoints = { 300, 150, 300 };
        g2D.setPaint(Color.MAGENTA);
        g2D.fillPolygon(xPoints, yPoints, 3);

        // String
        g2D.setFont(new Font("Minecraft", Font.BOLD, 28));
        g2D.setPaint(Color.ORANGE);
        g2D.drawString("HELLO WORLD", 5, 350);

        // Image
        g2D.drawImage(image, 5, 380, null);

    }

}
```