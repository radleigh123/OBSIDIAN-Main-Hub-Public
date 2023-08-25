---
cssclass:
aliases:
tags:
- Java
- Java/Collection/List/Stack
---
**[[Java#Collections|HOME [Java]]]**

---
## Stack Class
![[Pasted image 20230630105028.png|center wm-sm]]

a class that models and implements a Stack data structure. The class is based on the basic principle of last-in-first-out (**LIFO**). In addition to the basic `push` and `pop` operations.

Declaration: `public class Stack<E> extends Vector<E>`

<br>

Example: Stack implementation
>[!aside|right]-
> ```
> Pop Operation:
> 4
> 3
> 2
> 1
> 0
> Element on stack top: 4        
> Element is found at position: 3
> Element not found
> ```

```java
import java.io.*;
import java.util.*;

class Solution {
    // Pushing element on the top of the stack
    static void stack_push(Stack<Integer> stack) {
        for (int i = 0; i < 5; i++) {
            stack.push(i);
        }
    }

    // Popping element from the top of the stack
    static void stack_pop(Stack<Integer> stack) {
        System.out.println("Pop Operation:");

        for (int i = 0; i < 5; i++) {
            Integer y = (Integer) stack.pop();
            System.out.println(y);
        }
    }

    // Displaying element on the top of the stack
    static void stack_peek(Stack<Integer> stack) {
        Integer element = (Integer) stack.peek();
        System.out.println("Element on stack top: " + element);
    }

    // Searching element in the stack
    static void stack_search(Stack<Integer> stack, int element) {
        Integer pos = (Integer) stack.search(element);

        if (pos == -1)
            System.out.println("Element not found");
        else
            System.out.println("Element is found at position: " + pos);
    }

    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<Integer>();

        stack_push(stack);
        stack_pop(stack);
        stack_push(stack);
        stack_peek(stack);
        stack_search(stack, 2);
        stack_search(stack, 6);
    }
}

```

<br>

# 
---
- [Stack (Java SE 17 & JDK 17) (oracle.com)](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Stack.html)
- [Stack Class in Java - GeeksforGeeks](https://www.geeksforgeeks.org/stack-class-in-java/)
- **More on Stack Data Structure** - [Stack Data Structure - GeeksforGeeks](https://www.geeksforgeeks.org/stack-data-structure/)