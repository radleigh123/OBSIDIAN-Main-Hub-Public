---
aliases:
tags:
---
**[[COMPROG12LEC|MAINHUB]]**

---
## Understanding Method Construction
Every method must include the two parts featured in Figure 3-6:
-   A method header—A method’s header provides information about how other methods can interact with it. A method header is also called a declaration.
-   A method body between a pair of curly braces—The method body contains the statements that carry out the work of the method. A method’s body is called its implementation. Technically, a method is not required to contain any statements in its body, but you usually would have no reason to create an empty method in a class. Sometimes, while developing a program, the programmer creates an empty method as a placeholder and fills in the implementation later. An empty method is called a **stub**.

![[COMPROG12LECPRELIMch32image0.png|center]]

The method header is the first line of a method. It contains the following:
-   Optional access specifiers
-   A return type
-   An identifier
-   Parentheses

The next few figures compare these parts of a method header for the main() method and the `displayAddress()` method in the First class.

**Access Specifiers**
Figure 3-7 highlights the optional access specifiers for the two methods in the First class. The access specifier for a Java method can be any of the following modifiers: public, private, protected, or, if left unspecified, package by default. Most often, methods are given public access; this book will cover the other modifiers later. Endowing a method with public access means that any other class can use it, not just the class in which the method resides.

![[COMPROG12LECPRELIMch32image1.png|center]]

In addition, any method that can be used without instantiating an object requires the keyword modifier static. The main() method in an application must use the keyword static, but other methods, like `displayAddress()`, can use it too. You will learn about nonstatic methods later in this chapter.

**Return Type**
Figure 3-8 features the return types for the main() and `displayAddress()` methods in the First class. A return type describes the type of data the method sends back to its calling method. Not all methods return a value to their calling methods; a method that returns no data has a return type of void. The main() method in an application must have a return type of void; in this example, `displayAddress()` also has a void return type. Other methods that you will see later in this chapter have different return types. The phrases void method and method of type void both refer to a method that has a void return type.

![[COMPROG12LECPRELIMch32image2.png|center]]

**Method Name**
Figure 3-9 highlights the names of the two methods in the First class. A method’s name can be any legal identifier. That is, like identifiers for classes and variables, a method’s identifier must be one word with no embedded spaces, and cannot be a Java keyword. The method that executes first when you run an application must be named `main()`, but you have a lot of leeway in naming other methods that you create. Technically, you could even name another method main() as long as you did not include `String[]` within the parentheses, but doing so would be confusing and is not recommended. Because methods “do” something—that is, perform an action—their names frequently contain a verb, such as print or display.

![[COMPROG12LECPRELIMch32image3.png|center]]

**Parentheses**
As Figure 3-10 shows, every method header contains a set of parentheses that follow the identifier. The parentheses might contain data to be sent to the method. For example, when you write a main() method in a class, the parentheses in its header surround `String[] args`. The `displayAddress()` method in the First class requires no outside data, so its parentheses are empty. Later in this chapter, you will see several methods that accept data.

![[COMPROG12LECPRELIMch32image4.png|center]]

The full name of the `displayAddress()` method is `First.displayAddress()`, which includes the class name (First), a dot, and the method name, which is `displayAddress()`. (The name does not include an object because `displayAddress()` is a static method.) A complete name that includes the class is a fully qualified identifier. When you use a method within its own class, you do not need to use the fully qualified name (although you can); the simple method name alone is enough. However, if you want to use a method in another class, the compiler does not recognize the method unless you use the full name. You have used similar syntax (including a class name, dot, and method name) when calling the `JOptionPane.showMessageDialog()` method.

Each of two different classes can have its own method named `displayAddress()`. Such a method in the second class would be entirely distinct from the identically named method in the first class. You could use both methods in a third class by using their fully qualified identifiers. Two classes in an application cannot have the same name.