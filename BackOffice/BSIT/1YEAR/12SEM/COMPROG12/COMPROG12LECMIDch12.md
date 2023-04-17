---
cssclass:
aliases:
tags:
---
**[[COMPROG12LEC|MAINHUB]]**

---
## Creating a `for loop`
A `for loop` is a special loop that is used when a definite number of loop iterations is required; it provides a convenient way to create a counter-controlled loop. Although a while loop can also be used to meet this requirement, the for loop provides you with a shorthand notation for this type of loop. When you use a for loop, you can indicate the starting value for the loop control variable, the test condition that controls loop entry, and the expression that alters the loop control variable—all in one convenient place.

You begin a for loop with the keyword for followed by a set of parentheses. Within the parentheses are three sections separated by exactly two semicolons. The three sections are usually used for the following:
-   Initializing the loop control variable
-   Testing the loop control variable
-   Updating the loop control variable

The body of the for statement follows the parentheses. As with an if statement or a while loop, you can use a single statement as the body of a for loop, or you can use a block of statements enclosed in curly braces. Many programmers recommend that you always use a set of curly braces to surround the body of a for loop for clarity, even when the body contains only a single statement. You should use the conventions recommended by your organization.

Assuming that a variable named `val` has been declared as an integer, the for statement shown in Figure 6-18 produces the same output as the while statement shown below it—both display the integers 1 through 10.

![[COMPROG12LECMIDch12.png|center]]

Within the parentheses of the for statement shown in Figure 6-18, the first section prior to the first semicolon initializes `val` to 1. The program executes this statement once, no matter how many times the body of the for loop executes.

After initialization, program control passes to the middle, or test section, of the for statement that lies between the two semicolons. If the Boolean expression found there evaluates to true, the body of the for loop is entered. In the program segment shown in Figure 6-18, `val` initially is set to 1, so when `val < 11` is tested, it evaluates to true. The loop body displays val. In this example, the loop body is a single statement, so no curly braces are needed (although they could be added).

After the loop body executes, the final one-third of the for loop that follows the second semicolon executes, and `val` is increased to 2. Following the third section in the for statement, program control returns to the second section, where `val` is compared to 11 a second time. Because `val` is still less than 11, the body executes: `val` (now 2) is displayed, and then the third, altering portion of the for loop executes again. The variable `val` increases to 3, and the for loop continues. Eventually, when `val` is not less than 11 (after 1 through 10 have been displayed), the for loop ends, and the program continues with any statements that follow the for loop.

**Unconventional for Loops**
Although the three sections of the for loop are most commonly used to hold single expressions for initializing, testing, and incrementing, you can also perform the following tasks:

$\quad$◾ Initialization of more than one variable in the first section of the for statement by placing commas between the separate statements, as in the following:
```java
for(g = 0, h = 1; g < 6; ++g)
```

$\quad$◾ You can declare a variable within a for statement, as in the following:
```java
for(int val = 1; val < 11; ++val)
```

Programmers often use this technique when the loop control variable is not needed in any other part of the program. If you declare a variable within a for statement, the variable can only be used in the block that depends on the for statement; when the block ends, the variable goes out of scope.

$\quad$◾ Performance of more than one test using compound conditions in the second section, as in the following:
```java
for(g = 0; g < 3 && h > 1; ++g)
```

$\quad$◾ Decrementation or performance of some other task in the third section, as in the following:
```java
for(g = 5; g >= 1; ––g)
```

$\quad$◾ Performing multiple actions in the third section, separated by commas, as in the following:
```java
for(g = 0; g < 10; ++g, ++h, sum += g)
```

$\quad$◾ You might use method calls in any section of the for statement, as in the following example. Here, the `isFinished()` method would be required to return a Boolean value and the `alter()` method would be required to return a data type accepted by x.
```java
for(x = initMethod(); isFinished(); x = alter(x))
```

$\quad$◾ You can leave one or more portions of a for loop empty, although the two semicolons are still required as placeholders. For example, if `x` has been initialized in a previous program statement, you might write the following:
```java
for(; x < 10; ++x)
```

You might encounter for loops in which all three sections of the for statement are left empty. For example, consider the Clock class in Figure 6-19. The program contains a for loop that is meant to execute infinitely and display a clock with an updated time every second. Within the loop, the current time is retrieved using the `LocalDateTime` class. If the `getSecond()` value has changed since the last loop execution, the hour, minute, and second are displayed and the `prevSec` variable is updated. Figure 6-20 shows a typical execution; the user stopped the program after several seconds by holding down the Ctrl key and pressing C.

![[COMPROG12LECMIDch121.png|center]]

In general, you should use the same loop control variable in all three parts of a for statement, although you might see some programs written by others in which this is not the case. You should also avoid altering the loop control variable in the body of the loop. If a variable is altered both within a for statement and within the block it controls, it can be very difficult to follow the program’s logic. This technique can also produce program bugs that are hard to find. Usually, you should use the for loop for its intended purpose—as a shorthand way of programming a definite loop.

Occasionally, you will encounter a for loop that contains no body, but was purposely written that way, such as the following:
```java
for(x = 0; x < 100000; ++x);
```
Notice the final semicolon in this statement. This loop is a do-nothing loop that performs no actions in its body. It simply uses time—that is, it occupies the central processing unit for thousands of processing cycles because a brief pause is desired during program execution. As with if and while statements, usually you do not want to place a semicolon at the end of the for statement before the body of the loop. Java also contains a built-in method to pause program execution. The sleep() method is part of the Thread class in the `java.lang` package, and the time for which it pauses is more accurate than using a for loop. You will learn how to use the method as you continue to study Java.