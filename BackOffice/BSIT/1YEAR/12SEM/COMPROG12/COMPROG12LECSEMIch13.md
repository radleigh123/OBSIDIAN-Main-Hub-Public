---
cssclass:
aliases:
tags:
---
**[[COMPROG12LEC|MAINHUB]]**

---
## Using Variable Subscripts with an Array
If you treat each array element as an individual entity, there isn’t much of an advantage to declaring an array over declaring individual primitive type variables, such as those with the type int, double, or char. The power of arrays becomes apparent when you begin to use subscripts that are variables, rather than subscripts that are constant values.

For example, suppose you declare an array of five integers that holds quiz scores, such as the following:
```java
int[] scoreArray = {2, 14, 35, 67, 85};
```
You might want to perform the same operation on each array element, such as increasing each score by a constant amount. To increase each scoreArray element by three points, for example, you can write the following:
```java
final int INCREASE = 3;
scoreArray[0] += INCREASE;
scoreArray[1] += INCREASE;
scoreArray[2] += INCREASE;
scoreArray[3] += INCREASE;
scoreArray[4] += INCREASE;
```
With five `scoreArray` elements, this task is manageable, requiring only five statements. However, you can reduce the amount of program code needed by using a variable as the subscript. Then, you can use a loop to perform arithmetic on each array element, as in the following example:
```java
final int INCREASE = 3;
for(sub = 0; sub < 5; ++sub)
	scoreArray[sub] += INCREASE;
```
The loop control variable sub is set to 0, and then it is compared to 5. Because the value of sub is less than 5, the loop executes and 3 is added to `scoreArray[0]`. Then, the variable sub is incremented and it becomes 1, which is still less than 5, so when the loop executes again, `scoreArray[1]` is increased by 3, and so on. A process that took five statements now takes only one. In addition, if the array had 100 elements, the first method of increasing the array values by 3 in separate statements would result in 95 additional statements. The only changes required using the second method would be to change the array size to 100 by inserting additional initial values for the scores, and to change the middle portion of the for statement to compare sub to 100 instead of to 5. The loop to increase 100 separate scores by 3 each is:
```java
for(sub = 0; sub < 100; ++sub)
      scoreArray[sub] += INCREASE;
```
When an application contains an array and you want to use every element of the array in some task, it is common to perform loops that vary the loop control variable from 0 to one less than the size of the array. For example, if you get input values for the elements in the array, alter every value in the array, sum all the values in the array, or display every element in the array, you need to perform a loop that executes the same number of times as there are elements. (If you perform the loop too many times, the subscript will be out of bounds; if you do not perform the loop enough times, you will miss processing some elements in the list.) When there are 10 array elements, the subscript varies from 0 through 9; when there are 800 elements, the subscript varies from 0 through 799. Therefore, in an application that includes an array, it is convenient to declare a named constant equal to the size of the array and use it as a limiting value in every loop that processes the array. That way, if the array size changes in the future, you need to modify only the value stored in the named, symbolic constant, and you do not need to search for and modify the limiting value in every loop that processes the array.

For example, suppose you declare an array and a named constant as follows:
```java
int[] scoreArray = {2, 14, 35, 67, 85};
final int NUMBER_OF_SCORES = 5;
```
Then, the following two loops are identical:
```java
/*
 * for(sub = 0; sub < 5; ++sub)
 *     scoreArray[sub] += INCREASE;
 */

for(sub = 0; sub < NUMBER_OF_SCORES; ++sub)
	scoreArray[sub] += INCREASE;
```
The second format has two advantages. First, by using the named constant, `NUMBER_OF_SCORES`, the reader understands that you are processing every array element for the size of the entire array. If you use the number 5, the reader must look back to the array declaration to confirm that 5 represents the full size of the array. Second, if the array size changes because you remove or add scores, you change the named constant value only once, and all loops that use the constant are automatically altered to perform the correct number of repetitions.

As an even better option, you can use a field (instance variable) that is automatically assigned a value for every array you create; the length field contains the number of elements in the array. For example, when you declare an array using either of the following statements, the field `scoreArray.length` is assigned the value 5:
```java
int[] scoreArray = {2, 14, 35, 67, 85};
int[] scoreArray = new int[5];
```
Therefore, you can use the following loop to add 3 to every array element:
```java
for(sub = 0; sub < scoreArray.length; ++sub)
      scoreArray[sub] += INCREASE;
```
Later, if you modify the size of the array and recompile the program, the value in the length field of the array changes appropriately.When you work with array elements, it is always better to use a named constant or the length field when writing a loop that manipulates an array.

A frequent programmer error is to attempt to use length as an array method, referring to `scoreArray.length()`. As you learned in the last chapter, `length()` is a String method. However, length is not an array method; it is a field. An instance variable or object field such as length is also called a property of the object.

**Using the Enhanced for Loop**
Java also supports an enhanced for loop. This loop allows you to cycle through an array without specifying the starting and ending points for the loop control variable. For example, you can use either of the following statements to display every element in an array named `scoreArray`: 
```java
for(int sub = 0; sub < scoreArray.length; ++sub)
    System.out.println(scoreArray[sub]);
for(int val : scoreArray)
    System.out.println(val);
```
In the second example, val is defined to be the same type as the array named following the colon. Within the loop, `val` takes on, in turn, each value in the array. You can read the second example as, “*For each `val` in `scoreArray`, display val.*” As a matter of fact, you will see the enhanced for loop referred to as a `foreach loop`.

You also can use the enhanced for loop with more complicated Java objects, as you will see in the next section.

**Using Part of an Array**
Sometimes, you do not want to use every value in an array. For example, suppose that you write a program that allows a student to enter up to 10 quiz scores and then computes and displays the average. To allow for 10 quiz scores, you create an array that can hold 10 values, but because the student might enter fewer than 10 values, you might use only part of the array. Figure 8-4 shows such a program.

![[COMPROG12LECSEMIch13.png|center]]
![[COMPROG12LECSEMIch131.png|center]]

The `AverageOfQuizzes` program declares an array that can hold 10 quiz scores. The user is prompted for a first quiz score; then, a while loop starts and continues as long as the user does not enter 999, as shown in the first shaded line in Figure 8-4. Within the loop, the entered score is placed in the scores array, the score is added to a running total, and the count of scores entered is incremented. If the score just entered is the tenth score, the score is forced to 999 and the loop ends; otherwise, the user is prompted for the next score. The while loop continuously checks to ensure that the user has not entered 999 to quit. When the loop eventually ends, count holds the number of scores entered. The variable count then can be used to control the output loop (in the shaded for statement) and to calculate the average score (the last shaded portion in Figure 8-4). Figure 8-5 shows two typical executions of the program.