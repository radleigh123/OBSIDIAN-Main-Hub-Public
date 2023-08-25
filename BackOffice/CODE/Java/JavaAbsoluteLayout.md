---
cssclass:
aliases:
tags:
- Java
- Java/java.awt
- Java/javax.swing
---
**[[Java#Introduction Graphical User Interface (GUI)|HOME [Java]]]**

---
## Containers with Absolute Layout
If you want a container’s content to remain the same regardless of the window’s size, set the **x** and **y** coordinates, **width**, and **height** (aka the `bounds`) of each component while adding them to the window. Your class has to explicitly state that it won’t use any layout manager by passing null to `setLayout()`:
```java
windowContent.setLayout(null);
```
The next code snippet shows how you can set a [[JavaGUISwingJButton|button]]’s width to 40 pixels and its height to 20, and place it 100 pixels to the right of and 200 pixels down from the top left corner of the window:
```java
JButton button = new JButton("New Game");
button.setBounds(100, 100, 40, 20);
```