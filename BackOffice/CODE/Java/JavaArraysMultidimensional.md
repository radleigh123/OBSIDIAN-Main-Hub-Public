---
aliases:
tags:
- Java
- Java/Lecture
- Java/Arrays/Multidimensional
---
**[[JavaArrays|BACK]]**

---
## Multidimensional Arrays
(an array of arrays)

**Declaring and Initializing 2D Array**
```java
int[][] arr = { {1,2,3},
                {4,5,6} };

// declaring and initializing
String[][] stringValues;
stringValues = new String[][] {{"working", "with"}, {"2D", "arrays"}, {"is", "fun"}};
```
<br>

**Traversing w/ Enhanced for loop**
```java
for(String[] rowOfStrings : twoDStringArray) {
    for(String s : rowOfStrings) {
        System.out.print(s);
    }
    System.out.println();
}
/*
* In Java, enhanced for loops can be used to traverse 2D arrays. Because enhanced for loops have no index
* variable, they are better used in situations where you only care about the values of the 2D array - not
* the location of those values
*/
```

<br>

# 
---
- https://www.codecademy.com/learn/learn-java/modules/java-two-dimensional-arrays/cheatsheet