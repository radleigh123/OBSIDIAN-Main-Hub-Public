---
cssclass:
- t-w
- table-nalt
title: JavaMethodReference
creation-date: 2023-08-06
aliases:
tags:
- Java
- Java/MethodReference
---
**[[Java#Java 8 Stream API|HOME [Java]]]**

---
# Method Reference (`double colon` operator)
also known as **method reference operator** in Java, is used to call a method by referring to it with the help of its class directly. They behave exactly as the lambda expressions. The only difference it has from lambda expressions is that this uses direct reference to the method by name instead of providing a delegate to the method.
> i.e., used to **refer method of the functional interface**. It is compact and easy form of the lambda expression.

**Kinds of Method References**

| <center>Kind</center>                                                       | <center>Syntax</center>                | <center>Examples</center>                 |
| --------------------------------------------------------------------------- | -------------------------------------- | ----------------------------------------- |
| Reference to a static method                                                | `ContainingClass::staticMethodName`    | `Person::compareByAge`                    |
|                                                                             |                                        | `MethodReferencesExamples::appendStrings` |
|                                                                             |                                        |                                           |
| Reference to an instance method of a particular object                      | `containingObject::instanceMethodName` | `myComparisonProvider::compareByName`     |
|                                                                             |                                        | `myApp::appendStrings2`                   |
|                                                                             |                                        |                                           |
| Reference to an instance method of an arbitrary object of a particular type | `ContainingType::methodName`           | `String::compareToIgnoreCase`             |
|                                                                             |                                        | `String::concat`                          |
|                                                                             |                                        |                                           |
| Reference to a constructor                                                  | `ClassName::new`                       | `HashSet::new`                            |

>[!aside|right]-
> ```
> 6.0
> HELLO WORLD
> venus mars
> SET: [1, 2, 3, 4, 5]
> ```

```java
// 1. Reference to a static method
Function<Integer, Double> func = Math::sqrt;
// equivalent to: `func = i -> Math.sqrt(i)

System.out.println(func.apply(36));

// 2. Reference to an instance method of an object
Solution solution = new Solution();
Printable printable = solution::upper;
// equivalent to: s -> solution.upper(s)

printable.print("Hello World");

// 3. Reference to an instance method of an arbitrary object of a particular type
Function<String, String> func2 = String::toLowerCase;
// equivalent to: s -> s.toLowerCase()

System.out.println(func2.apply("Venus MARS"));

// 4. Constructor reference
List<Integer> numbers = new ArrayList<>();
numbers.addAll(Arrays.asList(1, 2, 3, 4, 5));
Function<List<Integer>, Set<Integer>> listFunc = HashSet::new;
// equivalent to: listFunc = num -> new HashSet<>(num)

System.out.println("SET: " + listFunc.apply(numbers));


public void upper(String s) {  
	s = s.toUpperCase();  
	System.out.println(s);  
}
```

<br>

# 
---
- [Method References (The Java™ Tutorials > Learning the Java Language > Classes and Objects) (oracle.com)](https://docs.oracle.com/javase/tutorial/java/javaOO/methodreferences.html)
- [Method References in Java with examples - GeeksforGeeks](https://www.geeksforgeeks.org/method-references-in-java-with-examples/)