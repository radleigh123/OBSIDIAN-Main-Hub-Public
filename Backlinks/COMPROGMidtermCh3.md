>[!TIP] # Pseudocode
>- is an informal high-level description of the operating principle of a computer program or other algorithm.
>- is one method of designing or planning a program.
>- is used for documenting the program or module design (also known as the algorithm).
>- **Pseudo** means false, thus pseudocode means false code. A better translation would be the word fake or imitation. Pseudocode is fake (not the real thing).
>>[!EXAMPLE]- **Outline using Pseudocode**
>>**Input**
>> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; display a message asking the user to enter the first age
>> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; get the first age from the keyboard
>> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; display a message asking the user to enter the second age
>> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; get the second age from the keyboard
>>**Processing**
>> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; calculate the answer by adding the two ages together and dividing by two
>>**Output**
>> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; display the answer on the screen
>> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; pause so the user can see the answer**

## Writing your first C program
>[!NOTE] ![[Pasted image 20221013195804.png]]

<br>

## Comments in C Programming
>[!NOTE]- **Single Line Comment**
> Starts with two forward slashes ( **//** ) any text between **//** and the end of the line is ignored by the compiler (will not be executed).
>>[!EXAMPLE] // This is a comment

>[!NOTE]- **Multi Line Comment**
> Multi-line comments start with **/*** and ends with ***/** Any text between **/*** and ***/** will be ignored by the compiler.
>>[!EXAMPLE] **/*** This is for the multi line comment ***/**

<br>

## Variable Name Rules
>[!ATTENTION] 
>- Should not be a reserved word like int, double, printf, scanf etc.
>- Should start with a letter or an  underscore(_)
>- Can contain letters, numbers or  underscore
>- No other special characters are allowed  including space
>- Variable names are case sensitive

<br>

## Input and Output
>[!NOTE] ### **Output in C programming:**
> To output values or print text in C, you can use the `printf()` function. Example:
> ![[Pasted image 20221013195804.png]]
> 
>>[!EXAMPLE]- In order to have a new line of your output you must use **\n** inside the printf function.
>> ![[Pasted image 20221013200657.png|50%]]

>[!NOTE] ### **Input in C programming**
> You have already learned that `printf()` is used to **output values** in C. To get **user input**, you can use the `scanf()` function.
> ![[Pasted image 20221013200108.png]]
> 
>>[!WARNING]- NOTE
>> **Always** remember that we use **%d** if the variable datatype we are referring to is an **integer.** Hence, if it is a character we use **%c** if it is character, and **%f** if it is a float or double.
>>- **%d** - 3 **|** 5000 **|** 654 **|** 69
>>- **%f** -  3.15 **|** 5000.88 **|** 654.312 **|** 69.56843
>>- **%c** - 'a' **|** 'A' **|** 'C' **|** 'h' **|** 'Z'

<br>

## Operators
>[!NOTE] ### Arithmetic Operators
> Arithmetic operators are used to perform common mathematical operations.
> ![[Pasted image 20221013210233.png]]

>[!NOTE] ### Logical Operators
> Logical operators are used to determine the logic between variables or values:
> ![[Pasted image 20221013210304.png]]![[Pasted image 20221013210314.png]]

## If Else
>[!NOTE] ### Conditions and If statements
> You learned from the **operators comparison chapter**, that C supports the usual logical conditions from mathematics:
>- Less than: a < b
>- Less than or equal to: a <= b
>- Greater than: a > b
>- Greater than or equal to: a >= b
>- Equal to a == b
>- Not Equal to: a != b
>
>C has the following conditional statements:
>- Use if to specify a block of code to be executed, if a specified condition is true
>- Use else to specify a block of code to be executed, if the same condition is false
>- Use else if to specify a new condition to test, if the first condition is false
>
>>[!EXAMPLE] #### Syntax
>> if (condition) {
>> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *// block of code to be executed if the condition is true*
>> } else {
>> 
>> }
>
>>[!EXAMPLE]- #### If Else Example (1)
>>if (20 > 18) {
>>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; printf("20 is greater than 18");
>>}
>
>>[!EXAMPLE]- #### If Else Example (2)
>>![[Pasted image 20221013211212.png]]
>
>>[!EXAMPLE]- #### NESTED If Else Example
>>![[Pasted image 20221013211233.png]]

## Nested If Example

<br>

# 
---
**[BACK](COMPROG11LEC#^COMPROGMIDCH3)**