---
aliases:
tags:
- Java
- Java/Lecture
- Java/javax.swing
- Java/JFileChooser
---
**[[JavaSwing|BACK]]**

---
## `JFileChooser` class
> provides a simple mechanism for the user to choose a file

The object of `JFileChooser` class represents a dialog window from which the user can select file. It inherits [[JavaJComponent|JComponent]] class.

**Open/Save a file example**
>[!aside|show-title right]+ Result:
> ![[Pasted image 20230228160530.png|cover ws-med]]

```java
import java.io.*;

import javax.swing.*;
import javax.swing.filechooser.FileSystemView;

public class Proto {
    public static void main(String[] args) {
        JFileChooser jFile = new JFileChooser(FileSystemView.getFileSystemView().getHomeDirectory());

        int returnValue = jFile.showOpenDialog(null);

        if (returnValue == JFileChooser.APPROVE_OPTION) {
            File selectedFile = jFile.getSelectedFile();
            System.out.println(selectedFile.getAbsolutePath());
        }
    }
}
```

More examples:
- [[JavaGUISwingJFileChoosersample|Using an `ActionListener`]]

<br>

# 
---
- [JFileChooser (Java Platform SE 7)](https://docs.oracle.com/javase/7/docs/api/javax/swing/JFileChooser.html)
	- **[How to use File Choosers](https://docs.oracle.com/javase/tutorial/uiswing/components/filechooser.html)**
- https://www.javatpoint.com/java-jfilechooser
- **More information** - https://mkyong.com/swing/java-swing-jfilechooser-example/