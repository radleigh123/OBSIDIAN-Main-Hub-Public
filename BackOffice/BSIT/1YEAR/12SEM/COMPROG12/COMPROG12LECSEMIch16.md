---
cssclass:
aliases:
tags:
---
**[[COMPROG12LEC|MAINHUB]]**

---
## Two-Dimensional Arrays
When you declare an array such as `int[] someNumbers = new int[3];`, you can envision the three declared integers as a column of numbers in memory, as shown in Figure 9-8. In other words, you can picture the three declared numbers stacked one on top of the next. An array that you can picture as a column of values, and whose elements you can access using a single subscript, is a one-dimensional or single-dimensional array. You can think of the size of the array as its height. 

Java also supports two-dimensional arrays. Two-dimensional arrays have two or more columns of values, as shown in Figure 9-9. The two dimensions represent the height and width of the array. Another way to picture a two-dimensional array is as an array of arrays. It is easiest to picture two-dimensional arrays as having both rows and columns. You must use two subscripts when you access an element in a two-dimensional array. When mathematicians use a two-dimensional array, they often call it a matrix or a table; you might have used a two-dimensional array called a spreadsheet.

![[COMPROG12LECSEMIch16.png|center]]
![[COMPROG12LECSEMIch161.png|center]]

When you declare a one-dimensional array, you type a set of square brackets after the array’s data type. To declare a two-dimensional array in Java, you type two sets of brackets after the array type. For example, the array in Figure 9-9 can be declared as follows, creating an array named someNumbers that holds three rows and four columns:  
```java
int[][] someNumbers = new int[3][4];
```
Just as with a one-dimensional array, if you do not provide values for the elements in a two-dimensional numeric array, the values default to zero. You can assign other values to the array elements later. For example, `someNumbers[0][0] = 14;` assigns the value 14 to the element of the `someNumbers` array that is in the first column of the first row. Alternatively, you can initialize a two-dimensional array with values when it is created. For example, the following code assigns values to `someNumbers` when it is created:

![[COMPROG12LECSEMIch162.png]]

The someNumbers array contains three rows and four columns. You do not need to place each row of values for a two-dimensional array on its own line. However, doing so makes the positions of values easier to understand. You contain the entire set of values within an outer pair of curly braces. The first row of the array holds the four integers 8, 9, 10, and 11. Notice that these four integers are placed within their own inner set of curly braces to indicate that they constitute one row, or the first row, which is row 0. Similarly, 1, 3, 12, and 15 make up the second row (row 1), which you reference with the subscript 1. Next, 5, 9, 44, and 99 are the values in the third row (row 2), which you reference with the subscript 2. The value of `someNumbers[0][0]` is 8. The value of `someNumbers[0][1]` is 9. The value of `someNumbers[2][3]` is 99. The value within the first set of brackets following the array name always refers to the row; the value within the second brackets refers to the column.

As an example of how useful two-dimensional arrays can be, assume that you own an apartment building with four floors—a basement, which you refer to as floor zero, and three other floors numbered one, two, and three. In addition, each of the floors has studio (with no bedroom) and one- and two-bedroom apartments. The monthly rent for each type of apartment is different—the higher the floor, the higher the rent (the view is better), and the rent is higher for apartments with more bedrooms. Table 9-1 shows the rental amounts.

![[COMPROG12LECSEMIch163.png|center]]

To determine a tenant’s rent, you need to know two pieces of information: the floor on which the tenant rents an apartment and the number of bedrooms in the apartment. Within a Java program, you can declare an array of rents using the following code:
![[COMPROG12LECSEMIch164.png]]

If you declare two integers named floor and bedrooms, then any tenant’s rent can be referred to as `rents[floor][bedrooms]`. Figure 9-10 shows an application that prompts a user for a floor number and number of bedrooms. Figure 9-11 shows a typical execution.

![[COMPROG12LECSEMIch165.png|center]]
![[COMPROG12LECSEMIch166.png|center]]

**Passing a Two-Dimensional Array to a Method**
When you pass a two-dimensional array to a method, you pass the array name just as you do with a one-dimensional array. A method that receives a two-dimensional array uses two bracket pairs following the data type in the parameter list of the method header. For example, the following method headers accept two-dimensional arrays of ints, doubles, and Employees, respectively:
```java
public static void displayScores(int[][] scoresArray)  
public static boolean areAllPricesHigh(double[][] prices)  
public static double computePayrollForAllEmployees(Employee[][] staff)  
```
In each case, notice that the brackets indicating the array in the method header are empty. There is no need to insert numbers into the brackets because each passed array name is a starting memory address. The way you manipulate subscripts within the method determines how rows and columns are accessed.

**Using the length Field with a Two-Dimensional Array**
You learned that a one-dimensional array has a length field that holds the number of elements in the array. With a two-dimensional array, the length field holds the number of rows in the array. Each row, in turn, has a length field that holds the number of columns in the row. For example, suppose you declare a rents array as follows:
![[COMPROG12LECSEMIch167.png]]

The value of `rents.length` is 4 because there are four rows in the array. The value of `rents[0].length` is 3 because there are three columns in the first row of the rents array. Similarly, the value of `rents[1].length` also is 3 because there are three columns in the second row.

Figure 9-12 shows an application that uses the length fields associated with the rents array to display all the rents. The floor variable varies from 0 through one less than 4 in the outer loop, and the bdrms variable varies from 0 through one less than 3 in the inner loop. Figure 9-13 shows the output.

![[COMPROG12LECSEMIch168.png|center]]
![[COMPROG12LECSEMIch169.png|center]]

**Understanding Ragged Arrays**
In a two-dimensional array, each row also is an array. In Java, you can declare each row to have a different length. When a two-dimensional array has rows of different lengths, it is a ragged array because you can picture the ends of each row as uneven. You create a ragged array by defining the number of rows for a two-dimensional array, but not defining the number of columns in the rows. For example, suppose that you have four sales representatives, each of whom covers a different number of states as their sales territory. Further suppose that you want an array to store total sales for each state for each sales representative. You would define the array as follows:
```java
double[][] sales = new double[4][];
```
This statement declares an array with four rows, but the rows are not yet created. Then, you can declare the individual rows, based on the number of states covered by each salesperson as follows:
```java
sales[0] = new double[12];  
sales[1] = new double[18];  
sales[2] = new double[9];  
sales[3] = new double[11];
```