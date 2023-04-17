---
cssclass:
aliases:
tags:
---
**[[COMPROG12LEC|MAINHUB]]**

---
## Learning About Nested Loops
Just as if statements can be nested, so can loops. You can place a while loop within a while loop, a for loop within a for loop, a while loop within a for loop, or any other combination. When loops are nested, each pair contains an inner loop and an outer loop. The inner loop must be entirely contained within the outer loop; loops can never overlap. Figure 6-25 shows a diagram in which the shaded inner loop is nested within an outer loop. You can nest virtually any number of loops; however, at some point, your machine will no longer be able to store all the necessary looping information.

![[COMPROG12LECMIDch15.png|center]]

Suppose you want to display future bank balances while varying both years and interest rates. Figure 6-26 shows an application that contains an outer loop that varies interest rates between specified limits. At the start of the outer loop, the working balance is reset to its initial value so that calculations are correct for each revised interest rate value. The shaded inner loop varies the number of years and displays each calculated balance. Figure 6-27 shows a typical execution.

![[COMPROG12LECMIDch151.png|center]]

When you nest loops, sometimes it doesn’t make any difference which variable controls the outer loop and which variable controls the inner one, but frequently it does make a difference. When you use a loop within a loop, you should always think of the outer loop as the all-encompassing loop. The variable in the outer loop changes more infrequently. For example, suppose a method named `outputLabel()` creates customer mailing labels in three different colors to use in successive promotional mailings, and that the color value is stored as an integer. The following nested loop calls the `outputLabel()` method 60 times and produces three labels for the first customer, three labels for the second customer, and so on:
```java
for(customer = 1; customer <= 20; ++customer)
	for(color = 1; color <= 3; ++color)
		outputLabel();
```
The following nested loop also calls outputLabel() 60 times, and it ultimately produces the same 60 labels, but it creates 20 labels in the first color, 20 labels in the second color, and then 20 labels in the third color.
```java
for(color = 1; color <= 3; ++color)
	for(customer = 1; customer <= 20; ++customer)
		outputLabel();
```
If changing the ink color is a time-consuming process that occurs in the outputLabel() method, the second nested loop might execute much faster than the first one.