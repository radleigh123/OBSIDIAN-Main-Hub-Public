---
aliases:
tags:
- Java
- Java/Lecture
- Java/Methods/Overriding
- Java/Override
- Java/Class
---
**[[JavaMethod|BACK]]**

---
## Method Overriding
> when subclass method is marked with the `@Override` annotation, it tells the compiler to check if it overrides in the **superclass**.

is a feature that allows a subclass to provide a different implementation of a [[JavaMethod|method]] that is already defined in its superclass. Method overriding comes in handy in the following situations:
- The source code of the superclass is not available, but you still need to change its functionality.
- The original version of the method is still valid in some cases and you want to keep it intact.
- To enable [[JavaPolymorphism|polymorphism]].

<br>

Example:
- [[JavaMethodsOverridingsample0|Bank Scenario program]]

<br>

# 
---
- https://www.javatpoint.com/method-overriding-in-java