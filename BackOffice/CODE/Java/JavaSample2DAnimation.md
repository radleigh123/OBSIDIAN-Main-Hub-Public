---
cssclass:
aliases:
tags:
- Java
- Java/Lecture
- Java/javax.swing
- Java/java.awt
- Java/java.awt.event
- Java/JFrame
- Java/Image
- Java/Timer
---
**[[Java|HOME [Java]]]**

---
## 2D Animations
>[!aside|show-title right]+ RESULT:
> ![[JavaSample2DAnimationimage.png|center]]

```java
public class Proto {
    public static void main(String[] args) {
        new myFrame();
    }
}
```
```java
import java.awt.*;
import javax.swing.*;

public class myFrame extends JFrame {

    myPanel panel;

    myFrame() {

        panel = new myPanel();

        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        this.add(panel);
        this.pack();
        this.setLocationRelativeTo(null);
        this.setVisible(true);

    }

}
```
```java
import java.awt.*;
import java.awt.event.*;

import javax.swing.*;

public class myPanel extends JPanel implements ActionListener {

    final int PANEL_WIDTH = 500;
    final int PANEL_HEIGHT = 281;
    Image arrowImage;
    Image backgroundImage;
    Timer timer;

    // adjust how many pixels image will be moving
    int xVelocity = 5;
    int yVelocity = 2;
    int x = 0;
    int y = 0;

    myPanel() {

        this.setPreferredSize(new Dimension(PANEL_WIDTH, PANEL_HEIGHT));
        this.setBackground(Color.MAGENTA);

        arrowImage = new ImageIcon("play.png").getImage(); // make an image out of the `ImageIcon`
        backgroundImage = new ImageIcon("forestBackground.jpg").getImage();

        timer = new Timer(2, this); // since class is implementing, `this` is used
        timer.start();

    }

    public void paint(Graphics g) {

        super.paint(g); // paint the background

        Graphics2D G2D = (Graphics2D) g;

        G2D.drawImage(backgroundImage, 0, 0, null);
        G2D.drawImage(arrowImage, x, y, null);
    }

    @Override
    public void actionPerformed(ActionEvent e) {

        if ((x >= PANEL_WIDTH - arrowImage.getWidth(null)) || x < 0) {
            xVelocity *= -1;
        }

        if ((y >= PANEL_HEIGHT - arrowImage.getHeight(null)) || y < 0) {
            yVelocity *= -1;
        }

        x += xVelocity;
        y += yVelocity;
        repaint(); // call paint() again

    }

}
```