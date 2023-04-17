---
cssclass:
aliases:
tags:
---
**[[COMPROG12LEC|MAINHUB]]**

---
## Learning How and When to Use a `do`…`while Loop`
With all the loops you have written so far, the loop body might execute many times, but it is also possible that the loop will not execute at all. For example, recall the bank balance program that displays compound interest, which was shown in Figure 6-8. The program begins by asking whether the user wants to see next year’s balance. If the user doesn’t enter a 1 for yes, the loop body never executes.

Similarly, recall the EnterSmallValue application in Figure 6-10. The user is prompted to enter a value, and if the user enters a value that is 3 or less, the error-reporting loop body never executes.

In each of these cases, the loop control variable is evaluated at the “top” of the loop before the body has a chance to execute. Both while loops and for loops are pretest loops—ones in which the loop control variable is tested before the loop body executes.

Sometimes, you might need to ensure that a loop body executes at least one time. If so, you want to write a loop that checks at the “bottom” of the loop after the first iteration. The do…while loop is such a loop; it is a posttest loop—one in which the loop control variable is tested after the loop body executes.

Figure 6-22 shows the general structure of a do…while loop. Notice that the loop body executes before the loop-controlling question is asked even one time. In other words, the decision is at the end of the loop body, making this a posttest loop. Figure 6-23 shows a BankBalance2 application that contains a do…while loop. The loop starts with the shaded keyword do. The body of the loop follows and is contained within curly braces. The first year’s balance is output before the user has any option of responding. At the bottom of the loop, the user is prompted, “Do you want to see the balance at the end of another year?” Now the user has the option of seeing more balances, but viewing the first display was unavoidable. The user’s response is checked in the shaded evaluation at the bottom of the loop; if it is 1 for yes, the loop repeats. Figure 6-24 shows a typical execution.
>[!grid|alt-co]
> ![[COMPROG12LECMIDch14.png]]
> ![[COMPROG12LECMIDch141.png]]

When the body of a do…while loop contains a single statement, you do not need to use curly braces to block the statement. For example, the following loop correctly adds numberValue to total while total remains less than 200:
```java
do
	total += numberValue;
while(total < 200);
```
Even though curly braces are not required in this case, many programmers recommend using them. Doing so prevents the third line of code from looking like it should begin a new while loop instead of ending the previous do…while loop. Therefore, even though the result is the same, the following example that includes curly braces is less likely to be misunderstood by a reader:
```java
do {
	total += numberValue;
} while(total < 200);
```
You are never required to use a do…while loop. In the bank balance example, you could achieve the same results as the logic shown in Figure 6-23 by unconditionally displaying the first year’s bank balance once before starting the loop, prompting the user, and then starting a while loop that might not be entered. However, when you know you want to perform some task at least one time, the do…while loop is convenient.