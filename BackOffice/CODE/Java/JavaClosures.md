---
cssclass:
aliases:
tags:
- Java
- Java/Class/Inner
- Java/Class/Closure
- Java/Lambda
---
**[[Java#Event Handling in UI|HOME [Java]]]**

---
## Closures
>[!WARNING|no-t txt-c alt-co collapse]
> Pre-requisite of learning the **Java closure**, is to understand [[JavaLambda|lambda expression]] in Java.

$\quad$is a method that refers to **free variables** in their lexical context. A free variable is an identifier used but not defined by the closure. It can be used without being a method or a class. It means that closure can access variables that are not defined in the parameter list and also assigned to a variable. We can also parse the closure as a parameter.

$\quad$In other words, a lambda expression becomes a closure when it is able to access the variables that are outside of this scope. It means a lambda can access its outer scope.
```java
// SYNTAX:
(argument_list) -> {function_body}
```

<br>

**Closure** vs **Lambda**
Java lambda expression is a way to define a function inline rather than the standard method of declaration. It provides a concise way to represent a function. While closure is a function that encompasses its surrounding state by referencing fields that are external to its body. Note that both are functions but **not all closures are lambdas** and **not all lambdas are closures**.

The difference between closure and lambda is quite equivalent to the distinction between a class and an instance of the class. A class exists only in source code. it doesn't exist at runtime. What exists at runtime are objects of the class type. Closures are to lambdas as objects are to classes. The following table describes the key differences between closure and lambda.

<br>

# 
---
- https://www.javatpoint.com/java-closure
- https://www.geeksforgeeks.org/closures-in-java-with-examples/