---
aliases:
tags:
- Java
- Java/javax.swing
- Java/java.awt
- Java/java.awt.event
- Java/MouseEvent
- Java/MouseListener
- Java/MouseMotionListener
- Java/Graphics/paintIcon
- Java/Graphics/paintComponent
- Java/Point
- Java/repaint
- Java/translate
---
**[[Java|HOME [Java]]]**

---
## Drag and Drop Images
![[JavaSampleDrag&DropImagesimage.png|cover center wsmall]]

**main**
```java
public class Proto {
    public static void main(String[] args) {
        myFrame myframe = new myFrame();
    }
}
```
**myFrame**
```java
import javax.swing.JFrame;

public class myFrame extends JFrame {

    DragPanel dragpanel = new DragPanel();

    myFrame() {

        this.add(dragpanel);
        this.setTitle("Drag and Drop Demo");
        this.setSize(600, 500);
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        this.setVisible(true);

    }

}
```
**DragPanel**
```java
import java.awt.*;
import java.awt.event.*;

import javax.swing.ImageIcon;
import javax.swing.JPanel;

public class DragPanel extends JPanel {

    ImageIcon image = new ImageIcon("play.png");
    final int WIDTH = image.getIconWidth();
    final int HEIGHT = image.getIconHeight();
    Point imageCorner;
    Point prevPoint;

    DragPanel() {

        imageCorner = new Point(0, 0);
        ClickListener clicklistener = new ClickListener();
        DragListener draglistener = new DragListener();

        // adding for events
        this.addMouseListener(clicklistener);
        this.addMouseMotionListener(draglistener);

    }

    public void paintComponent(Graphics g) {

        super.paintComponent(g);
        image.paintIcon(this, g, ((int) imageCorner.getX()), ((int) imageCorner.getY()));

    }

    private class ClickListener extends MouseAdapter {

        public void mousePressed(MouseEvent e) {
            prevPoint = e.getPoint(); // updates the previous points clicked
        }

    }

    private class DragListener extends MouseMotionAdapter {

        public void mouseDragged(MouseEvent e) {
            Point currentPoint = e.getPoint();

            imageCorner.translate(
                    (int) (currentPoint.getX() - prevPoint.getX()),
                    (int) (currentPoint.getY() - prevPoint.getY()));

            prevPoint = currentPoint;

            repaint();
        }

    }

}
```