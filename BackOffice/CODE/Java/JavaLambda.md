---
cssclass:
title: JavaLambda
creation-date: 2023-07-01
aliases:
tags:
- Java
- Java/Lambda 
---
**[[Java#Java 8 Stream API|HOME [Java]]]**

---
# *Java 8*: Lambda Expressions
One issue with anonymous classes is that if the implementation of your anonymous class is very simple, such as an interface that contains only one method, then the syntax of anonymous classes may seem unwieldy and unclear. In these cases, you're usually trying to pass functionality as an argument to another method, such as what action should be taken when someone clicks a button. Lambda expressions enable you to do this, to treat functionality as method argument, or code as data.

Although this is often more concise than a named class, for classes with only one method, even an anonymous class seems a bit excessive and cumbersome. Lambda expressions let you **express instances of single-method classes more compactly**.

>[!DONE|ttl-c] REMEMBER
> The behavior of functions that handle elements in a Java stream, **cannot change the values of variables outside of the function**. This is because, during a method call, there is no access to any variables outside of the method. However, **the values of variables outside the function can be read**, as long as those values do not change in the program.

Syntax:
```
parameter -> expression
```
```
(parameter1, parameter2) -> expression
```
```
(parameter1, parameter2) -> { code block }
```
![[JavaLambda.png|center wm-sm]]

>[!INFO|ttl-c txt-c]
> To invoke <u>lambda expressions</u>, a functional [[JavaInterface|interface]] must be defined.
> A functional interface is **an interface that contains only one abstract method**. They can have only one functionality to exhibit.

<br>

# 
---
- [Java Lambda Expressions (w3schools.com)](https://www.w3schools.com/java/java_lambda.asp)
- [Lambda Expressions (oracle.com)](https://docs.oracle.com/javase/tutorial/java/javaOO/lambdaexpressions.html)