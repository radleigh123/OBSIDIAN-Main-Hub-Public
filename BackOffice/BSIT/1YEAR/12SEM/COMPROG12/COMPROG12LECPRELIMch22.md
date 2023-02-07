---
aliases:
tags:
---
**[[COMPROG12LEC|BACK]]**

---
## Java Data Types
**Learning About Integer Data Types**
In Java, you can use variables of data types byte, short, int, and long to store (or hold) integers; an integer is a whole number without decimal places.

![[COMPROG12LECPRELIMch22image0.png]]

**Using the boolean Data Type**
Boolean logic is based on true or false comparisons.Whereas an int variable can hold millions of different values (at different times), a boolean variable can hold only one of two values—true or false. The following statements declare and assign appropriate values to Boolean variables:

boolean isItPayday = false;  
boolean areYouBroke = true;  

Although you can use any legal identifier for Boolean variables, they are easily identified as Boolean if you use a form of to be (such as is or are) as part of the variable name, as in isItPayday.

Besides assigning true and false, you also can assign a value to a Boolean variable based on the result of a comparison. Java supports six relational operators that are used to make comparisons. A relational operator compares two items; it is sometimes called a comparison operator. The value of an expression that contains a relational operator is always true or false. 

**Learning About Floating-Point Data Types**
A floating-point number contains decimal positions. Java supports two floating-point data types: float and double. A float data type can hold floating-point values of up to six or seven significant digits of accuracy. A double data type requires more memory than a float, and can hold 14 or 15 significant digits of accuracy. The term significant digits refer to the mathematical accuracy of a value. For example, a float given the value 0.324616777 is displayed as 0.324617 because the value is accurate only to the sixth decimal position. Table 2-4 shows the minimum and maximum values for each floating-point data type. Notice that the maximum value for a double is 3.4 * 10 to the 38th power, which means 3.4 times 10 with 38 trailing zeros—a very large number.

Depending on the environment in which you run your program, a float given the value 324616777 is displayed using a decimal point after the 3 and only six or seven digits followed by e+008 or E8. This format is called scientific notation, and means that the value is approximately 3.24617 times 10 to the 8th power, or 324617000. The e in the displayed value stands for exponent; the 8 means the true decimal point is eight positions to the right of where it is displayed, indicating a very large number. (A negative number following the e would mean that the true decimal point belongs to the left, indicating a very small number.)

A programmer might choose to store a value as a float instead of a double to save memory. However, if high levels of accuracy are needed, such as in graphics-intensive software, the programmer might choose to use a double, opting for high accuracy over saved memory.

**Using the char Data Type**
You use the char data type to hold any single character. You place constant character values within single quotation marks because the computer stores characters and integers differently. For example, the following are typical character declarations:

char middleInitial = 'M';  
char gradeInChemistry = 'A';  
char aStar = '*';  

A character can be any letter—uppercase or lowercase. It might also be a punctuation mark or digit. A character that is a digit is represented in computer memory differently than a numeric value represented by the same digit.