---
aliases:
tags:
- Java
- Java/java.awt
- Java/GridBagLayout
- Java/GridBagConstraints
---
**[[JavaSwing|BACK]]**

---
## `GridBagLayout` class
![[JavaLayoutMangerGridBag.png|right wm-sm]]
is an advanced grid that allows cells of different sizes. *GridBagLayout* works with another class called `GridBagConstraints`.

>[!INFO|clean no-t collapse alt-co]
> Constraints are just attributes of a cell, and you have to set them for each cell separately. All constraints for a cell have to be set before you place a component in the cell. For example, one of the constraint’s attributes is called `gridwidth`. It allows you to make a cell as wide as several other cells.

When working with the grid layout you should create an instance of the constraint object first, and then set the values to its properties. Then you can add a UI component to the cell in your container.

Example:
▪$\,$[[JavaLayoutMangerGridBagSample|Creating constraints for GridBagLayout]]

<br>

# 
---
- [How to Use GridBagLayout](https://docs.oracle.com/javase/tutorial/uiswing/layout/gridbag.html)