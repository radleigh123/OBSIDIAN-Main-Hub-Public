---
cssclass:
aliases:
tags:
- Java
- Java/Class/Anonymous
---
**[[UpdateJava#Java 8 Stream API|HOME [Java]]]**

---
## Anonymous Class
these enable you to make your code more concise. They enable you to declare and instantiate a class at the same time. They are like local classes except that they do not have a name.
> *Use them if you need to use a local class only once.*

#### Declaring Anonymous Classes
While local classes are class declarations, anonymous classes are expressions, which means that you define the class in another expression.
>[!aside|right]-
> ```
> Hello
> Ola
> ```

```java
interface HelloWorld {
    public void greet();
}
```
```java
public class Solution {

    public Solution() {
        sayHello();
    }

    public void sayHello() {
	    // anonymous class
		HelloWorld frenchGreeting = new HelloWorld() {
            public void greet() {
                System.out.println("Ola");
            }
        };

		// local class
        class EnglishGreeting implements HelloWorld {
            public void greet() {
                System.out.println("Hello");
            }
        }

        HelloWorld englishGreeting = new EnglishGreeting();

        englishGreeting.greet();
        frenchGreeting.greet();
    }

    public static void main(String... args) {
        Solution myApp = new Solution();
    }
}
```

<br>

#### Syntax of Anonymous Classes
The syntax of an anonymous class expression is like the invocation of a constructor, except that there is a class definition contained in a block of code. Consider the instantiation of the `frenchGreeting` object (source code above).
```
Object objectName = new Type(parameter) {
	 // body
};
```
The anonymous class expression consists of the following:
- The `new` operator
- The name of an interface to implement or a class to extend. In this example, the anonymous class is implementing the interface `HelloWorld`.
- Parentheses that contain the arguments to a constructor, just like a normal class instance creation expression. **Note**: <mark class="hltr-lightgreen">When you implement an interface, there is no constructor, so you use an empty pair of parentheses `()`</mark>
- A body, which is a class declaration body. More specifically, in the body, [[JavaMethod|method declarations]] are allowed but [[JavaTerminologies|statements]] are not.

Because an anonymous class definition is an expression, it must be part of a statement. In this example, the anonymous class expression is part of the statement that instantiates the `frenchGreeting` object. (This explains why there is a semicolon after the closing brace.)

<br>

# 
---
- [Anonymous Classes (The Java™ Tutorials > Learning the Java Language > Classes and Objects) (oracle.com)](https://docs.oracle.com/javase/tutorial/java/javaOO/anonymousclasses.html)