---
cssclass:
aliases:
tags:
- Java
---
**[[Java#Introduction Graphical User Interface (GUI)|HOME [Java]]]**

---
## Top-Level Containers & Containment Hierarchies
$\quad$Each program that uses Swing components has at least one top-level container. This top-level container is the root of a containment hierarchy — the hierarchy that contains all of the Swing components that appear inside the top-level container.

$\quad$As a rule, a standalone application with a Swing-based GUI has at least one containment hierarchy with a [[JavaGUISwingJFrame|JFrame]] as its root. For example, if an application has one main window and two dialogs, then the application has three containment hierarchies, and thus three top-level containers. One containment hierarchy has a **JFrame** as its root, and each of the other two has a [[JavaSwingJDialog|JDialog]] object as its root.

$\quad$A Swing-based applet has at least one containment hierarchy, exactly one of which is rooted by a [[JavaSwingJApplet|JApplet]] object. For example, an applet that brings up a dialog has two containment hierarchies. The components in the browser window are in a containment hierarchy rooted by a **JApplet** object. The dialog has a containment hierarchy rooted by a **JDialog** object.

<br>

# 
---
- https://docs.oracle.com/javase/tutorial/uiswing/components/toplevel.html