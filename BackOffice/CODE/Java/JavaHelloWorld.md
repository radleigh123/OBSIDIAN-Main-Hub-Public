---
cssclass:
- tag-outline
aliases:
tags:
- Java
---
**[[Java|HOME [Java]]]**

---
## Hello World Program
```java
public class Main {

    public static void main(String[] args) {
    
	    int num1;       // declaration
	    num1 = 555;     // assignment
	    int num2 = 444; // initialization
	    
        System.out.println("Hello" + " " + "World");
        
    }

}
```

#Java/Class/AccessModifier/public #Java/static #Java/void #Java/String 
This method signature includes the access level (public), instructions on usage (static), return value type (void), name of the method (main), and argument list (String[] args).
- The keyword `public` means that the method `main()` can be accessed by any other Java class.
- The keyword [[Javastatic|static]] means that you don’t have to create an instance of this class to use this method.
- The keyword `void` means that the method `main()` doesn’t return any value to the calling program.
- The keyword `String[] args` tells us that this method will receive an array of characters as the argument (you can pass external data to this method from a command line)