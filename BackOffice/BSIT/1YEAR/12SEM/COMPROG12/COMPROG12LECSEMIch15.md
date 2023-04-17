---
cssclass:
aliases:
tags:
---
**[[COMPROG12LEC|MAINHUB]]**

---
## Passing Arrays to and Returning Arrays from Methods
You have already seen that you can use any individual array element in the same manner as you use any single variable of the same type. That is, if you declare an integer array as `int[] someNums = new int[12];`, you can subsequently display `someNums[0]`, or increment `someNums[1]`, or work with any element just as you do for any integer. Similarly, you can pass a single array element to a method in exactly the same manner as you pass any variable.

Examine the `PassArrayElement` application shown in Figure 8-16 and the output shown in Figure 8-17. The application creates an array of four integers and displays them. Then, the application calls the `methodGetsOneInt()` method four times, passing each element in turn. The method displays the number, changes the number to 999, and then displays the number again. Finally, back in the main() method, the four numbers are displayed again.

![[COMPROG12LECSEMIch15.png|center]]
![[COMPROG12LECSEMIch151.png|center]]

As you can see in Figure 8-17, the four numbers that were changed in the `methodGetsOneInt()` method remain unchanged back in main() after the method executes. The variable named one is local to the `methodGetsOneInt()` method, and any changes to variables passed into the method are not permanent and are not reflected in the array in the main() program. Each variable named one in the `methodGetsOneInt()` method holds only a copy of the array element passed into the method. The individual array elements are passed by value; that is, a copy of the value is made and used within the receiving method. When any primitive type (boolean, char, byte, short, int, long, float, or double) is passed to a method, the value is passed.

Arrays, like all nonprimitive objects, are reference types; this means that the object actually holds a memory address where the values are stored. Because an array name is a reference, you cannot assign another array to it using the `=` operator, nor can you compare two arrays using the `==` operator. Additionally, when you pass an array (that is, pass its name) to a method, the receiving method gets a copy of the array’s actual memory address. This means that the receiving method has access to, and the ability to alter, the original values in the array elements in the calling method.

The class shown in Figure 8-18 creates an array of four integers. After the integers are displayed, the array name (its address) is passed to a method named `methodGetsArray()`. Within the method, the numbers are displayed, which shows that they retain their values from `main()`, but then the value 888 is assigned to each number. Even though `methodGetsArray()` is a void method—meaning nothing is returned to the main() method—when the main() method displays the array for the second time, all of the values have been changed to 888, as you can see in the output in Figure 8-19. Because the method receives a reference to the array, the `methodGetsArray()` method “*knows*” the address of the array declared in main() and makes its changes directly to the original array.

![[COMPROG12LECSEMIch152.png|center]]
![[COMPROG12LECSEMIch153.png|center]]

Notice that in the first shaded statement in Figure 8-18, the array name is passed to the method and no brackets are used. In the method header, brackets are used to show that the parameter is an array of integers (a reference) and not a simple int.

![[COMPROG12LECSEMIch154.png|center]]

**Returning an Array from a Method**
A method can return an array reference. When a method returns an array reference, you include square brackets with the return type in the method header. For example, Figure 8-20 shows a `getArray()` method that returns a locally declared array of `int`'s. Square brackets are used as part of the return type; the return statement returns the array name without any brackets.

![[COMPROG12LECSEMIch155.png]]

When you call the `getArray()` method in Figure 8-20, you can store its returned value in any integer array reference. For example, you might declare an array and make the method call in the following statement:
```java
int[] scoresFromMethod = getArray();
```