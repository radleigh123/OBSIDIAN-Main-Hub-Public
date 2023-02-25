---
aliases:
tags:
- Java
- Java/Lecture
- Java/javax.swing
- Java/JOptionPane/showInputDialog
---
**[[JavaGUISwingJOptionPane|BACK]]**

---
## `showInputDialog`
- takes input
- **parameters:**
	- (`Component, Object, String, int`)
		- (returns `String`) shows a dialog requesting input from the user. The dialog has a title set through the String parameter and a *MessageType* set through the int parameter.
	- (`Component, Object, String, int, Icon, Object[], Object`)
		- (returns `Object`) prompts the user for input in a blocking dialog where the initial selection, possible selections, and all other options can be specified. The Icon (if not null) is displayed inside the dialog and overrides the default *MessageType* icon.

**Simple example**
```java
import javax.swing.JOptionPane;

public class SimpleInputDialog1 {

    public static void main(String[] args){

        String m = JOptionPane.showInputDialog("Anyone there?");
        System.out.println(m);

    }
}
```

>[!INFO|clean no-i]- **Complex example**
> <mark class="hltr-blue">Component, Object, String & int</mark>
>
>>[!aside|show-title right]+ Result:
>> ![[JavaGUISwingJOptionPaneshowInputDialogimage1.png|cover wsmall]]
>
> ```java
> import javax.swing.JOptionPane;
> 
> public class Proto {
> 
>     public static void main(String[] args) {
> 
>         String m = JOptionPane.showInputDialog(null, "Broccoli is tasty!",
>                 "Green dinner", JOptionPane.INFORMATION_MESSAGE);
> 
>         System.out.println(m);
> 
>     }
> }
> ```
> <mark class="hltr-blue">Component, Object, String, int, Icon, Object[] & Object</mark>
> 
>>[!aside|show-title right]+ Result:
>>![[JavaGUISwingJOptionPaneshowInputDialogimage2.png|cover wsmall]]
>
> ```java
> import javax.swing.*;
> 
> public class Proto {
>     public static void main(String[] args) {
> 
>         String[] options = { "I adore turtles", "Yes", "Maybe", "Urm...", "No", "Hate them" };
>         ImageIcon icon = new ImageIcon("src/images/turtle32.png");
>         String n = (String) JOptionPane.showInputDialog(null, "Do you like turtles??",
>                 "I like turtles", JOptionPane.QUESTION_MESSAGE, icon, options, options[2]);
>         System.out.println(n);
> 
>     }
> }
> ```

<br>

# 
---
- https://mkyong.com/swing/java-swing-joptionpane-showinputdialog-example/