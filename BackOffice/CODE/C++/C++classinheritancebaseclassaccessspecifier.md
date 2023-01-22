---
aliases:
tags:
- CPP/Lecture
- CPP/Class/BaseClassAccessSpecifier/public
- CPP/Class/BaseClassAccessSpecifier/private
- CPP/Class/BaseClassAccessSpecifier/protected
- CPP/Class/Inheritance
- CPP/Preprocessor/define
- CPP/Preprocessor/conditional/endif
- CPP/Preprocessor/conditional/ifndef
---
**[[C++|HOME [C++]]]**

---
## Base class access specifiers: Zooming in
In a parent-child relationship between classes, the class that is being derived from is called the **base class**, and the class that is being derived is called the **derived class**.
There are base class access specifiers in C++:
- **`public`** - members that are accessible to both the base class and the derived class.
- **`protected`** - members that are accessible to the base class and the derived class, but <mark class="hltr-lightred">not to other classes</mark>.
- **`private`** - members that are declared as private in the base class are <mark class="hltr-lightred">not accessible to the derived class</mark>. ^3b4258

![[C++classinheritancebaseclassaccessspecifierillu1.excalidraw.svg|center]]

**Example:**
- [[C++classinheritancebaseclassaccessspecifiersample0|Basic sample]]
- [[C++classinheritancebaseclassaccessspecifiersample1|Basic sample `protected` and `private` class]]
- [[C++classinheritancebaseclassaccessspecifiersample2|Class base access specifier across multiple files]]

>[!NOTE|alt-co justified] NOTE
> Through the base class access specifier, we can control how relaxed or constrained is the access of base class members from the derived class.