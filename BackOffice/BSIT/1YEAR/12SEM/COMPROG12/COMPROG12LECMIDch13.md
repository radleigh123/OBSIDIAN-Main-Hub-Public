---
cssclass:
aliases:
tags:
---
**[[COMPROG12LEC|MAINHUB]]**

---
## Creating `while loop`
You can use a `while loop` to execute a body of statements continually as long as the Boolean expression that controls entry into the loop continues to be true. In Java, a while loop consists of the keyword while followed by a Boolean expression within parentheses, followed by the body of the loop.

You can use a while loop when you need to perform a task either a predetermined or unpredictable number of times. A loop that executes a specific number of times is a definite loop or a counted loop. On the other hand, the number of times the loop executes might not be determined until the program is running. Such a loop is an indefinite loop because you don’t know how many times it will eventually loop.

**Writing a Definite while Loop**
To write a definite loop, you initialize a loop control variable, a variable whose value determines whether loop execution continues. While the Boolean value that results from comparing the loop control variable and another value is true, the body of the while loop continues to execute. In the body of the loop, you must include a statement that alters the loop control variable; otherwise, the loop will never end. For example, the program segment shown in Figure 6-2 displays the series of integers 1 through 10. The variable `lcv` is the loop control variable—it starts the loop holding a value of 1, and while the value remains under 11, `lcv` continues to be output and increased.

![[COMPROG12LECMIDch131.png|center]]

When you write applications containing loops, it is easy to make mistakes. For example, executing the code shown in Figure 6-3 causes the message “Hello” to be displayed forever ([[theoretically]]) because there is no code to end the loop. A loop that never ends is called an infinite loop.

![[COMPROG12LECMIDch132.png|center]]

In Figure 6-3, the expression `4 > 2` evaluates to true. You obviously never need to make such an evaluation, but if you do so in this while loop, the body of the loop is entered and “Hello” is displayed. Next, the expression is evaluated again. The expression `4 > 2` is still true, so the body is entered again. “Hello” is displayed repeatedly; the loop never finishes because `4 > 2` is never false.

It is a bad idea to write an infinite loop intentionally. However, even experienced programmers write them by accident. So, before you start writing loops, it is good to know how to exit from an infinite loop. You might suspect an infinite loop if the same output is displayed repeatedly, or if the screen simply remains idle for an extended period of time without displaying the expected output. If you think your application is in an infinite loop, you can press and hold the Ctrl key, and then press C or the Break key; the looping program should terminate. (On many keyboards, the Break key is also the Pause key.)

To prevent a while loop from executing infinitely, three separate actions must occur:
-   A loop control variable is initialized to a starting value.
-   The loop control variable is tested in the while statement.
-   The loop control variable is altered within the body of the loop. The variable must be altered so that the test expression can eventually evaluate to false and the loop can end.

All of these conditions are met by the example in Figure 6-4. First, a loop control variable `loopCount` is named and set to a value of 1. Second, `loopCount` is compared to 3. Third, `loopCount` is altered in the loop body when 1 is added to it. Note that the loop body shown in Figure 6-4 consists of two statements made into a block by their surrounding curly braces. When `loopCount` is 1, it is compared to 3, and because it is less than 3, the loop body executes, displaying “Hello” and increasing `loopCount`. The next time `loopCount` is evaluated, it is 2. It is still less than 3, so the loop body executes again. “Hello” is displayed a second time, and `loopCount` becomes 3. Finally, because the expression `loopCount < 3` now evaluates to false, the loop ends. Program execution then continues with any subsequent statements.

![[COMPROG12LECMIDch133.png|center]]

**Pitfall: Failing to Alter the Loop Control Variable Within the Loop Body**
It is important that the loop control variable be altered within the body of the loop. Figure 6-5 shows the same code as in Figure 6-4, but the curly braces have been eliminated. In this case, the while loop body ends at the semicolon that appears at the end of the “Hello” statement. Adding 1 to the `loopCount` is no longer part of a block that contains the loop, so the value of `loopCount` never changes, and an infinite loop is created.

![[COMPROG12LECMIDch134.png|center]]

**Pitfall: Unintentionally Creating a Loop with an Empty Body**
As with the decision-making if statement that you learned about in Chapter 5, placement of the statement-ending semicolon is important when you work with the while statement. If a semicolon is mistakenly placed at the end of the partial statement while(loopCount < 3);, as shown in Figure 6-6, the loop is also infinite. This loop has an empty body, or a body with no statements in it. So, the Boolean expression is evaluated, and because it is true, the loop body is entered. Because the loop body is empty, no action is taken, and the Boolean expression is evaluated again. Nothing has changed, so it is still true, the empty body is entered, and the infinite loop continues.

![[COMPROG12LECMIDch135.png|center]]

**Altering a Definite Loop’s Control Variable**
A definite loop is a counter-controlled loop because the loop control variable is changed by counting. It is very common to alter the value of a loop control variable by adding 1 to it, or incrementing the variable. However, not all loops are controlled by adding 1. The loop shown in Figure 6-7 displays “Hello” twice, just as the loop in Figure 6-4 does, but its loop is controlled by subtracting 1 from a loop control variable, or decrementing it.

![[COMPROG12LECMIDch136.png|center]]

In the program segment shown in Figure 6-7, the variable `loopCount` begins with a value of 3. The `loopCount` is greater than 1, so the loop body displays “Hello” and decrements `loopCount` to 2. The Boolean expression in the while loop is tested again. Because 2 is more than 1, “Hello” is displayed again, and `loopCount` becomes 1. Now `loopCount` is not greater than 1, so the loop ends. There are many ways to execute a loop two times. For example, you can initialize a loop control variable to 10 and continue while the value is greater than 8, decreasing the value by 1 each time you pass through the loop. Similarly, you can initialize the loop control variable to 12, continue while it is greater than 2, and decrease the value by 5 each time. In general, you should not use such unusual methods to count repetitions because they simply make a program confusing. To execute a loop a specific number of times, the clearest and best method is to start the loop control variable at 0 or 1, increment by 1 each time through the loop, and stop when the loop control variable reaches the appropriate limit.

**Writing an Indefinite while Loop**
You are not required to alter a loop control variable by adding to it or subtracting from it. Often, the value of a loop control variable is not altered by arithmetic, but instead is altered by user input. Instead of being a counter-controlled loop, an indefinite loop is an event-controlled loop. That is, an event occurs that determines whether the loop continues. An event-controlled loop is a type of indefinite loop because you don’t know how many times it will eventually repeat. For example, perhaps you want to continue asking a user questions as long as the response is correct. In this case, while you are writing the program, you do not know whether the loop eventually will be executed two times or 200 times.

Consider an application in which you ask the user for a bank balance and then ask whether the user wants to see the balance after interest has accumulated. Each time the user chooses to continue, an increased balance appears, reflecting one more year of accumulated interest. When the user finally chooses to exit, the program ends. The program appears in Figure 6-8.

![[COMPROG12LECMIDch137.png|center]]

The program shown in Figure 6-8 declares needed variables and a constant for a 3 percent interest rate, and then asks the user for a balance. The application then asks the user to enter 1 if the user wants see the next year’s balance. As long as the user wants to continue, the application continues to display increasing bank balances.

The loop in the application in Figure 6-8 begins with the line that contains:
```java
while(response == 1)
```
If the user enters any integer value other than 1, the loop body never executes; instead, the program ends. However, if the user enters 1, all the statements within the loop body execute. The application increases the balance by the interest rate value, displays the new balance, adds 1 to year, and asks whether the user wants another balance. The last statement in the loop body accepts the user’s response. After the loop body executes, control returns to the top of the loop, where the Boolean expression in the while loop is tested again. If the user’s response is 1, the loop is entered and the process begins again. Figure 6-9 shows the output of the `BankBalance` application after the user enters a starting balance and responds with 1 five times to the prompt for increased interest payments before responding 2. 

**Validating Data**
Programmers commonly use indefinite loops when validating input data. Validating data is the process of ensuring that a value falls within a specified range. For example, suppose you require a user to enter a value no greater than 3. Figure 6-10 shows an application that does not progress past the data entry loop until the user enters a correct value. If the user enters 3 or less at the first prompt, the shaded loop never executes. However, if the user enters a number greater than 3, the shaded loop executes, providing the user with another chance to enter a correct value. While the user continues to enter incorrect data, the loop repeats. Figure 6-11 shows a typical execution.

![[COMPROG12LECMIDch138.png|center]]

Figure 6-10 illustrates an excellent method for validating input. Before the loop is entered, the first input is retrieved. This first input might be a value that prevents any executions of the loop. This first input statement prior to the loop is called a priming read or priming input. Within the loop, the last statement retrieves subsequent input values for the same variable that will be checked at the entrance to the loop.

Novice programmers often make the mistake of checking for invalid data using a decision instead of a loop. That is, they ask whether the data is invalid using an if statement; if the data is invalid, they reprompt the user. However, they forget that a user might enter incorrect data multiple times. Usually, a loop is the best structure to use when validating input data.