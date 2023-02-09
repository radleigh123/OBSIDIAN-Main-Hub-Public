---
aliases:
tags:
- Java
- Java/Lecture
- Java/Arrays
- Java/java.util/Arrays/copyOfRange
---
**[[JavaArrays|BACK]]**

---
<center>package: <strong>java.util.Arrays</strong></center>

## Array Manipulation
Java SE provides several methods for performing array manipulations (common tasks, such as copying, sorting and searching arrays) in the `java.util.Arrays class`.
**e.g.**
```java
class ArrayCopyOfDemo {
    public static void main(String[] args) {
        String[] copyFrom = {
            "Affogato", "Americano", "Cappuccino", "Corretto", "Cortado",   
            "Doppio", "Espresso", "Frappucino", "Freddo", "Lungo", "Macchiato",      
            "Marocchino", "Ristretto" };
        
        String[] copyTo = java.util.Arrays.copyOfRange(copyFrom, 2, 9);        
        for (String coffee : copyTo) {
            System.out.print(coffee + " ");           
        }            
    }
}
```
**output:**
```
Cappuccino, Corretto, Cortado, Doppio, Espresso, Frappucino, Freddo
```
<br>

Some other useful operations provided by methods in the `java.util.Arrays` class are:
- Creating a stream that uses an array as its source (the stream method). For example, the following statement prints the contents of the copyTo array in the same way as in the previous example:
	- **java.util.Arrays.stream(copyTo).map(coffee -> coffee + " ").forEach(System.out::print);** 
- Converting an array to a string. The `toString` method converts each element of the array to a string, separates them with commas, then surrounds them with brackets. For example, the following statement converts the `copyTo` array to a string and prints it:
	- **System.out.println(java.util.Arrays.toString(copyTo));**

<br>

# 
---
- **[Java Arrays](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/arrays.html)**
- **[copyOfRange](https://www.tutorialspoint.com/java/util/arrays_copyofrange_short.htm)**