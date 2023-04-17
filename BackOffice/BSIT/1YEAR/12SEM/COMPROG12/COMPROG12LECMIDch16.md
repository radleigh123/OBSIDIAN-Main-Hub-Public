---
cssclass:
aliases:
tags:
---
**[[COMPROG12LEC|MAINHUB]]**

---
## Improving Loop Performance
Whether you decide to use a while, for, or do…while loop in an application, you can improve loop performance by doing the following:
-   Making sure the loop does not include unnecessary operations or statements
-   Considering the order of evaluation for short-circuit operators
-   Making a comparison to 0
-   Employing loop fusion to combine loops
-   Using prefix incrementing rather than postfix incrementing

If a loop only executes a few times, implementing the suggestions presented in this section won’t change program performance very much, but for a large-scale application in which speed is important, some of these suggestions can make a difference. Thinking about these suggestions also improves your understanding of how loops work.

**Avoiding Unnecessary Operations**
You can make loops more efficient by not using unnecessary operations or statements, either within a loop’s tested expression or within the loop body. For example, suppose a loop should execute while x is less than the sum of two integers, a and b. The loop could be written as:

![[COMPROG12LECMIDch16.png|center]]

If this loop executes 1,000 times, then the expression a + b is calculated 1,000 times. Instead, if you use the following code, the results are the same, but the arithmetic is performed only once:

![[COMPROG12LECMIDch161.png]]

Of course, if a or b is altered in the loop body, then a new sum must be calculated with every loop iteration. However, if the sum of a and b is fixed prior to the start of the loop, then writing the code the second way is far more efficient. 

Similarly, if the method getNumberOfEmployees() always returns the same value during a program’s execution, then a loop that begins as follows might unnecessarily call the method many times:
```java
while(count < getNumberOfEmployees())…
```
It is more efficient to call the method once, store the result in a variable, and use the variable in the repeated evaluations, as in this example: 
```java
numEmployees = getNumberOfEmployees();  
while(count < numEmployees)…
```
**Considering the Order of Evaluation of Short-Circuit Operators**
In making decisions, you learned that the operands in each part of an AND or an OR expression use short-circuit evaluation; that is, they are evaluated only as much as necessary to determine whether the entire expression is true or false. When a loop might execute many times, it becomes increasingly important to consider the number of evaluations that take place.

For example, suppose a user can request any number of printed copies of a report from 0 to 15, and you want to validate the user’s input before proceeding. If you believe that users are far more likely to enter a value that is too high than to enter a negative one, then you want to start a loop that reprompts the user with the following expression:
```java
while(requestedNum > LIMIT || requestedNum < 0)…
```
Because you believe that the first Boolean expression is more likely to be true than the second one, you can eliminate testing the second one on more occasions. The order of the expressions might not be very important in a single loop, but if this loop is nested within another loop, the difference in the number of comparisons increases. Similarly, when compound if statements are contained in a loop that might execute thousands of times, the order of the evaluations in if statements is more important than when the evaluation is made only once.

**Comparing to Zero**
Making a comparison to 0 is faster than making a comparison to any other value. Therefore, if your application makes comparison to 0 feasible, you can improve loop performance by structuring your loops to compare the loop control variable to 0 instead of some other value. For example, a loop that performs based on a variable that varies from 0 up to 100,000 executes the same number of times as a loop based on a variable that varies from 100,000 down to 0. However, the second loop performs slightly faster. Comparing a value to 0 instead of other values is faster because in a compiled language, condition flags for the comparison are set once, no matter how many times the loop executes. Comparing a value to 0 is faster than comparing to other values, no matter which comparison operator you use—greater than, less than, equal to, and so on.

Figure 6-29 contains a program that tests the execution times of two nested do-nothing loops, which are shaded in the figure. The program declares variables to hold a startTime before each nested loop begins and an endTime after each nested loop is complete. Before each nested loop execution, the current time is retrieved from the LocalDateTime class and the value of the nanoseconds (billionths of a second) is retrieved using the getNano() method. After each nested loop repeats 100,000 times, the current time is retrieved again. Subtracting one time from the other computes the interval, and dividing by 1 million converts nanoseconds to more readable milliseconds. As the execution in Figure 6-30 shows, there is a small difference in execution time between the two loops—about 1/20 of a second. The amount of time will vary on different machines, and varies for subsequent executions on the same machine depending on events occurring elsewhere on the machine during the same time period, but the loop that uses the 0 comparison will never be slower than the other one. The difference would become more pronounced with additional repetitions or further nesting levels. For example, if the value of the loop control variable was needed within the loops to display a count to the user, then you might be required to vary the loop starting with 0. However, if the purposes of the loops are just to count iterations, you might consider making the loop comparison use 0.

![[COMPROG12LECMIDch162.png|center]]

**Employing Loop Fusion**
Loop fusion is the technique of combining two loops into one. For example, suppose you want to call two methods 100 times each. You can set a constant named TIMES to 100 and use the following code:
```java
for(int x = 0; x < TIMES; ++x)  
	method1();
for(int x = 0; x < TIMES; ++x)  
	method2();
```
However, you can also use the following code:
```java
for(int x = 0; x < TIMES; ++x) { 
      method1();  
      method2();  
}  
```
Fusing loops will not work in every situation; sometimes all the activities for all the executions of `method1()` must be finished before those in `method2()` can begin. However, if the two methods do not depend on each other, fusing the loops can improve performance.

**Using Prefix Incrementing Rather than Postfix Incrementing**
Probably the most common action after the second semicolon in a for statement is to increment the loop control variable. In most textbooks and in many professional programs, the postfix increment operator is used for this purpose, as in the following:
```java
for(int x = 0; x < LIMIT; x++)
```
Because incrementing x is a stand-alone statement in the for loop, the result is identical whether you use x++ or ++x. However, using the prefix increment operator produces a faster loop. Consider the program in Figure 6-31. It is similar to the **CompareLoopTimes** application in Figure 6-29, but instead of comparing loops that count up and down, it compares loops that use prefix and postfix incrementing. The two timed, do-nothing loops that repeat 50,000 times each are shaded in the figure.

![[COMPROG12LECMIDch163.png|center]]

Figure 6-32 shows a typical execution of the program. The program that uses prefix incrementing runs slightly faster than the one that uses postfix incrementing because when the compiler uses postfix incrementing, it first makes a copy of the variable it uses as the expression’s value, and then it increments the variable. In other words, the operators are methods that behave as follows:
-   When you use the prefix incrementing method, as in ++x, the method receives a reference to x, increases it, and returns the increased value.
-   When you use the postfix incrementing method, as in x++, the method receives a reference to x, makes a copy of the value and stores it, increments the value indicated by the reference, and returns the copy. The extra time required to make the copy is what causes postfix incrementing to take longer.

![[COMPROG12LECMIDch164.png|center]]

As you can see in Figure 6-32, the difference in duration for 50,000 loops is very small—only 47/1000 of a second. If you run the program multiple times, you will get different results. However, using the prefix operator typically saves a small amount of time. As a professional, you will encounter programmers who insist on using either postfix or prefix increments in their loops. You should follow the conventions established by your organization, but now you have the tools to prove that prefix incrementing is faster.

---
**A Final Note on Improving Loop Performance**
In the previous sections, you have learned to improve loop performance by eliminating unnecessary operations, considering the order of evaluation for short-circuit operators, making comparisons to 0, employing loop fusion, and using prefix incrementing rather than postfix incrementing. As you become an experienced programmer, you will discover other ways to enhance the operation of the programs you write. You should always be on the lookout for ways to improve program performance. However, almost all business professionals agree that if saving a few milliseconds ends up making your code harder to understand, you have not succeeded. You almost always should err in favor of programs that are more readable and easier to maintain, even if they execute more slowly.