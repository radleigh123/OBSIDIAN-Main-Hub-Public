---
cssclass:
title: JavaUML
creation-date: 2023-08-09
aliases:
tags:
- Java
- Java/UML
---
**[[Java#Java Basics|HOME [Java]]]**

---
# Unified Modeling Language - UML
is a <u>general purpose modelling language</u>. The main aim of UML is to define a standard way to visualize the way a system has been designed. It is quite similar to blueprints used in other fields of engineering. UML is <mark class="hltr-lightred">not a programming language</mark>, it is rather a visual language.

### Class Diagram
is a graphical notation used to construct and visualize object oriented systems. A class diagram in the **UML** is a type of static structure diagram that describes the structure of a system by showing the system's:
- classes,
- their attributes,
- methods,
- and the relationship among objects.

>[!NOTE|ttl-c]+ A class diagram describes classes, constructors and methods.
> However a class diagram tells us nothing about the implementation of the constructors or the methods. Therefore a **class diagram describes the structure of an object but not its functionality**.
> 
> For example the method `printPerson` uses the class attributes `name` and `age`, but this cannot be seen from the class diagram.
> ![[Pasted image 20230809164424.png|center]]
> ```java
> public void printPerson() {
> 	System.out.println(this.name + ", age " +   this.age + " years");
> }
> ```

**UML Class Notation**
A class represent a concept which encapsulates state (attributes) and behavior (methods). Each attribute has a type. Each **method** has a **signature**. _The class name is the **only mandatory information**_.

![[Pasted image 20230809155735.png|center]]

<u>Class Name:</u>
▪ The name of the class appears in the first partition.

<u>Class Attributes:</u>
▪ Attributes are shown in the second partition.
▪ The attribute type is shown after the colon, e.g., `length : int`

<u>Class Methods:</u>
▪ Operations are shown in the third partition.. They are services the class provides.
▪ The return type of a method is shown after the colon at the end of the method signature.
▪ The return type of method parameters are shown after the colon following the parameter name.

![[Pasted image 20230809162944.png|center]]

**Class Visibility**
`+` - public attributes or operations
`-` - private attributes or operations
`#` - protected attributes or operations

**Parameter Directionality**
Each parameter in an operation (method) may be denoted as in, **out** or **inout** which specifies its direction with respect to the caller. This directionality is shown before the parameter name.

![[Pasted image 20230809163225.png|center]]

#### Perspectives of Class Diagram
> The choice of perspective depends on how far along you are in the development process.

During the formulation of a **domain model**, for example, you would seldom move past the **conceptual perspective**. **Analysis models** will typically feature a mix of **conceptual and specification perspectives**. **Design model** development will typically start with heavy emphasis on the **specification perspective**, and evolve into the **implementation perspective**.
A diagram can be interpreted from various perspectives:
- **Conceptual**: represents the concepts in the domain
- **Specification**: focus is on the interfaces of Abstract Data Type (ADTs) in the software
- **Implementation**: describes how classes will implement their interfaces

The perspective affects the amount of detail to be supplied and the kinds of relationships worth presenting. As we mentioned above, the class name is the only mandatory information.

![[Pasted image 20230809163557.png|center]]

<br>

> **How these should be drawn?**
> Class diagrams are an excellent way to describe a problem and a problem-domain to others. They are particularily useful when a programmer is designing a program with multiple classes.
> 
> Often a class diagram is drawn on a whiteboard or a large sheet of paper during the design phase. <mark class="hltr-lightgreen">Class diagrams should be thought of as helpful tools to build a program, which can be thrown away afterwards</mark>. You should not use too much energy to think about the correctness and details of the modeling language. Class diagrams should also be drawn in a suitable level of abstraction. For example, if you have tens of classes, it might not be worth describing each attribute and each method of each class; getting a good overview of the program structure is the most important.
> 
> The class diagrams can be drawn using **yUML**, **Creately**, and **draw.io**.

<br>

# 
---
- [UML Class Diagram Tutorial (visual-paradigm.com)](https://www.visual-paradigm.com/guide/uml-unified-modeling-language/uml-class-diagram-tutorial/)
- [Unified Modeling Language (UML) | An Introduction - GeeksforGeeks](https://www.geeksforgeeks.org/unified-modeling-language-uml-introduction/)
- [UML Class Diagram - Javatpoint](https://www.javatpoint.com/uml-class-diagram)