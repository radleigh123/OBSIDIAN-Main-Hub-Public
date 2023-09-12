---
cssclasses:
  - hide-header-underline-1
aliases: []
tags: []
---
**[[JavaFX|BACK]]**

---
## Application Structure
JavaFX application is divided hierarchically into three main components known as: Stage, Scene and, nodes.

**Stage**
Stage in a JavaFX application is similar to the **Frame** in a [[JavaSwing|Swing Application]]. It <mark class="hltr-lightgreen">acts like a container for all the JavaFX objects</mark>. Primary Stage is created internally by the platform. Other stages can further be created by the application. The object of primary stage is passed to **start** method. We need to call **show** method on the **primary stage object** in order to show our primary stage. Initially, the primary Stage looks like following.
> However, we can add various objects to this primary stage. The objects can only be added in a hierarchical way i.e. 
>1. first, scene graph will be added to this primaryStage and 
>2. then that scene graph may contain the nodes. 
>3. A node may be any object of the user's interface like text area, buttons, shapes, media, etc.

![[Pasted image 20230911205805.png|center]]

**Scene**
Scene actually holds all the physical contents (nodes) of a JavaFX application. Creating scene is necessary in order to visualize the contents on the stage.

**Scene Graph**
Scene Graph exists at the lowest level of the hierarchy. It can be seen as the collection of various nodes. 
> A **node** is the element which is visualized on the stage. It can be any button, text box, layout, image, radio button, check box, etc.

The nodes are implemented in a tree kind of structure. There is always one root in the scene graph. This will act as a parent node for all the other nodes present in the scene graph.

![[Pasted image 20230911210658.png|center]]

<br>

# 
---
- [JavaFX Application Structure - javatpoint](https://www.javatpoint.com/javafx-application-structure)