---
cssclass:
aliases:
tags:
---
**[[COMPROG12LEC|MAINHUB]]**

---
## Searching value in an Array
Suppose that a company manufactures 10 items. When a customer places an order for an item, you need to determine whether the item number on the order form is valid. When you want to determine whether a variable holds one of many valid values, one option is to use a series of if statements to compare the variable to a series of valid values. If valid item numbers are sequential, such as 101 through 110, the following simple if statement that uses a logical `AND` can verify the order number and set a Boolean field to true:
```java
final int LOW = 101;
final int HIGH = 110;
boolean validItem = false;
if(itemOrdered >= LOW && itemOrdered <= HIGH)
	validItem = true;
```
In this example, the Boolean field `validItem` is used as a flag—a variable that holds a value as an indicator of whether some condition has been met. If the valid item numbers are non-sequential—for example, 101, 108, 201, and so on—you can code the following deeply nested if statement or a lengthy `OR` comparison to determine the validity of an item number:
```java
if(itemOrdered == 101)
    validItem = true;
else if(itemOrdered == 108)
    validItem = true;
else if(itemOrdered == 201)
	validItem = true;

// and so on
```
Instead of a long series of if statements, a more elegant solution is to compare the `itemOrdered` variable to a list of values in an array, a process called searching an array. You can initialize the array with the valid values using the following statement, which creates exactly 10 array elements with subscripts 0 through 9:
```java
int[] validValues = {101, 108, 201, 213, 266, 304, 311, 409, 411, 412};
```
After the list of valid values is initialized, you can use a for statement to loop through the array, and set a Boolean variable to true when a match is found:
```java
for(int x = 0; x < validValues.length; ++x) {
      if(itemOrdered == validValues[x])
           validItem = true;
}
```
This simple for loop replaces the long series of if statements; it checks the `itemOrdered` value against each of the 10 array values in turn. Also, if a company carries 1,000 items instead of 10, nothing changes in the for statement—the value of `validValues.length` is updated automatically.

**Using Parallel Arrays**
As an added bonus, if you set up another array with the same number of elements and corresponding data, you can use the same subscript to access additional information. A parallel array is one with the same number of elements as another, and for which the values in corresponding elements are related. For example, if the 10 items your company carries have 10 different prices, you can set up an array to hold those prices as follows:
```java
double[] prices = {0.29, 1.23, 3.50, 0.69…};
```
The prices must appear in the same order as their corresponding item numbers in the `validValues` array. Now, the same for loop that finds the valid item number also finds the price, as shown in the application in Figure 8-9. In the shaded portion of the code, notice that when the ordered item’s number is found in the `validValues` array, the `itemPrice` value is “*pulled*” from the prices array. In other words, if the item number is found in the second position in the `validValues` array, you can find the correct price in the second position in the prices array. Figure 8-10 shows a typical execution of the program. A user requests item 409, which is the eighth element in the `validValues` array, so the price displayed is the eighth element in the prices array.

![[COMPROG12LECSEMIch14.png|center]]
![[COMPROG12LECSEMIch141.png|center]]

Within the code shown in Figure 8-9, you compare every `itemOrdered` with each of the 10 `validValues`. Even when an `itemOrdered` is equivalent to the first value in the `validValues` array (101), you always make nine additional cycles through the array. On each of these nine additional cycles, the comparison between `itemOrdered` and `validValues[x]` is always false. As soon as a match for an `itemOrdered` is found, it is most efficient to break out of the for loop early. An easy way to accomplish this is to set x to a high value within the block of statements executed when there is a match. Then, after a match, the for loop does not execute again because the limiting comparison `(x < NUMBER_OF_ITEMS)` is surpassed. Figure 8-11 shows this loop. In an array with many possible matches, it is most efficient to place the more common items first, so they are matched right away. For example, if item 311 is ordered most often, place 311 first in the `validValues` array, and place its price ($0.99) first in the prices array.

![[COMPROG12LECSEMIch143.png|center]]

In the code in Figure 8-11, the loop control variable is altered within the loop body. Some programmers object to altering a loop control variable within the body of a for loop; they feel that the loop control variable should only be altered in the third section of the for clause (where x is incremented). These programmers would prefer the loop in Figure 8-12, in which two Boolean expressions appear in the shaded section in the middle portion of the for clause. In this example, the loop control variable is not altered within the loop body. Instead, x must be within range before each iteration and `validItem` must not yet have been set to true.

![[COMPROG12LECSEMIch144.png|center]]

**Searching an Array for a Range Match**
Searching an array for an exact match is not always practical. Suppose your company gives customer discounts based on the quantity of items ordered. Perhaps no discount is given for any order of fewer than a dozen items, but there are increasing discounts available for orders of increasing quantities, as shown in Table 8-1.

![[COMPROG12LECSEMIch145.png|center]]

One awkward option is to create a single array to store the discount rates. You could use a variable named numOfItems as a subscript to the array, but the array would need hundreds of entries, as in the following example:
```java
double[] discounts = {0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0.10, 0.10, 0.10, …};
```
Thirteen zeroes are listed in the discounts array. The first array element has a 0 subscript and represents a zero discount for zero items. The next 12 discounts (for items 1 through 12) are also zero. When numOfItems is 13, `discounts[numOfItems]`, or `discounts[13]`, is 0.10. The array would store 37 copies of `0.10` for elements 13 through 49. The discounts array would need to be ridiculously large to hold an exact value for each possible quantity ordered.

A better option is to create two corresponding arrays and perform a range match, in which you compare a value to the endpoints of numerical ranges to find the category in which a value belongs. For example, one array can hold the five discount rates, and the other array can hold five discount range limits. The Total Quantity Ordered column in Table 8-1 shows five ranges. If you use only the first figure in each range, you can create an array that holds five low limits:
```java
int[] discountRangeLimits = {1, 13, 50, 100, 200};
```
A parallel array can hold the five discount rates:
```java
double[] discountRates = {0, 0.10, 0.14, 0.18, 0.20};
```
Then, starting at the last discountRangeLimits array element, for any `numOfItems` greater than or equal to `discountRangeLimits[4]`, the appropriate discount is `discounts[4]`. In other words, for any `numOrdered` less than `discountRangeLimits[4]`, you should decrement the subscript and look in a lower range. Figure 8-13 shows an application that uses the parallel arrays, and Figure 8-14 shows a typical execution of the program.

![[COMPROG12LECSEMIch146.png|center]]
![[COMPROG12LECSEMIch147.png|center]]