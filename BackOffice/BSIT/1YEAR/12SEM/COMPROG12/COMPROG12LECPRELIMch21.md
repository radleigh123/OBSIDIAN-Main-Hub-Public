---
aliases:
tags:
---
**[[COMPROG12LEC|BACK]]**

---
## Declaring and Using Constants and Values
A data item is constant when its value cannot be changed while a program is running. For example, when you include the following statement in a Java class, the number 459 is a constant:
```java
System.out.println(459);
```
Every time an application containing the constant 459 is executed, the value 459 is displayed. Programmers refer to a number like 459 in several ways:
-   It is a literal constant because its value is taken literally at each use.
-   It is a numeric constant as opposed to a character or string constant.
-   It is an unnamed constant as opposed to a named one, because no identifier is associated with it.

Instead of using constant data, you can set up a data item to be variable. A variable is a named memory location that can store a value. A variable can hold only one value at a time, but the value it holds can change. For example, if you create a variable named ovenTemperature, it might hold 0 when the application starts, later be altered to hold 350, and still later be altered to hold 400.

Whether a data item is variable or constant, in Java it always has a data type. An item’s data type describes the type of data that can be stored there, how much memory the item occupies, and what types of operations can be performed on the data. Java provides for eight primitive types of data. A primitive type is a simple data type. Java’s eight data types are described in Table 2-1. Later in this chapter, you will learn more specific information about several of these data types.

![[COMPROG12LECPRELIMch21image0.png|center wm-tl]]

The eight data types in Table 2-1 are called primitive because they are simple and uncomplicated. Primitive types also serve as the building blocks for more complex data types, called reference types, which hold memory addresses. 

**Declaring Variables**
A variable declaration is a statement that reserves a named memory location and includes the following:
-   A data type that identifies the type of data that the variable will store
-   An identifier that is the variable’s name
-   An optional assignment operator and assigned value, if you want a variable to contain an initial value
-   An ending semicolon

Variable names must be legal Java identifiers. (You learned the requirements for legal identifiers in Chapter 1.) Basically, a variable name must start with a letter and cannot be a reserved keyword. You must declare a variable before you can use it. You can declare a variable at any point before you use it, but it is common practice to declare variables first in a method and to place executable statements after the declarations. Java is a strongly typed language, or one in which each variable has a well-defined data type that limits the operations you can perform with it; strong typing implies that all variables must be declared before they can be used.

Variable names conventionally begin with lowercase letters to distinguish them from class names. However, as with class names, a program can compile without error even if names are constructed unconventionally. Beginning an identifier with a lowercase letter and capitalizing subsequent words within the identifier is a style known as camel casing. An identifier such as lastName resembles a camel because of the uppercase “hump” in the middle.

For example, the following declaration creates a conventionally named int variable, myAge, and assigns it an initial value of 25:

int myAge = 25;

This declaration is a complete, executable statement, so it ends with a semicolon. The equal sign ( = ) is the assignment operator. Any value to the right of the assignment operator is assigned to the memory location named on the left. An assignment made when you declare a variable is an initialization; an assignment made later is simply an assignment. Thus, the first statement that follows is an initialization, and the second is an assignment:

int myAge = 25;

myAge = 42;

You declare a variable just once in a method, but you might assign new values to it any number of times.

Note that an expression with a literal to the left of the assignment operator (such as 25 = myAge) is illegal. The assignment operator has right-to-left associativity. Associativity refers to the order in which values are used with operators. The associativity of every operator is either right-to-left or left-to-right. An identifier that can appear on the left side of an assignment operator sometimes is referred to as an lvalue, and an item that can appear only on the right side of an assignment operator is an rvalue. A variable can be used as an lvalue or an rvalue, but a literal constant can only be an rvalue.

When you declare a variable within a method but do not assign a value to it, it is an uninitialized variable. For example, the following variable declaration declares a variable of type int named myAge, but no value is assigned at the time of creation:

int myAge;

An uninitialized variable contains an unknown value called a garbage value. Java protects you from inadvertently using the garbage value that is stored in an uninitialized variable. For example, if you attempt to display garbage or use it as part of a calculation, you receive an error message stating that the variable might not have been initialized, and the program will not compile.

You can declare multiple variables of the same type in separate statements. You also can declare two or more variables of the same type in a single statement by separating the variable declarations with a comma, as shown in the following statement:

int height = 70, weight = 190;

By convention, many programmers declare each variable in its own separate statement, but some follow the convention of declaring multiple variables in the same statement if their purposes are closely related. Remember that even if a statement occupies multiple lines, the statement is not complete until the semicolon is reached.

You can declare as many variables in a statement as you want, as long as the variables are the same data type. However, if you want to declare variables of different types, you must use a separate statement for each type.

**Declaring Named Constants**
A variable is a named memory location for which the contents can change. If a named location’s value should not change during the execution of a program, you can create it to be a named constant. A named constant is also known as a symbolic constant. A named constant is similar to a variable in that it has a data type, a name, and a value. A named constant differs from a variable in several ways:
-   In its declaration statement, the data type of a named constant is preceded by the keyword final.
-   A named constant can be assigned a value only once, and then it cannot be changed later in the program. Usually, you initialize a named constant when you declare it; if you do not initialize the constant at the declaration, it is known as a blank final, and you can assign a value later. Either way, you must assign a value to a constant before it is used.
-   Although it is not a requirement, named constants conventionally are given identifiers using all uppercase letters, using underscores as needed to separate words.

For example, each of the following defines a conventionally named constant:
final int NUMBER_OF_DEPTS = 20;  
final double PI = 3.14159;  
final double TAX_RATE = 0.015;  
final string COMPANY = "ABC Manufacturing";  

You can use each of these named constants anywhere you use a variable of the same type, except on the left side of an assignment statement after the first value has been assigned. In other words, when it receives a value, a named constant is an lvalue, but after the assignment, a named constant is an rvalue.

A constant always has the same value within a program, so you might wonder why you should not use the actual, literal value. For example, why not use the unnamed constant 20 when you need the number of departments in a company rather than going to the trouble of creating the NUMBER_OF_DEPTS named constant? There are several good reasons to use the named constant rather than the literal one:
-   The number 20 is more easily recognized as the number of departments if it is associated with an identifier. Using named constants makes your programs easier to read and understand. Some programmers refer to the use of a literal numeric constant, such as 20, as using a magic number—a value that does not have immediate, intuitive meaning or a number that cannot be explained without additional knowledge. For example, you might write a program that uses the value 7 for several purposes, so you might use constants such as DAYS_IN_WEEK and NUM_RETAIL_OUTLETS that both hold the value 7 but more clearly describe the purposes. Avoiding magic numbers helps provide internal documentation for your programs.
-   If the number of departments in your organization changes, you would change the value of NUMBER_OF_DEPTS at one location within your program—where the constant is defined— rather than searching for every use of 20 to change it to a different number. Being able to make the change at one location saves you time, and prevents you from missing a reference to the number of departments.
-   Even if you are willing to search for every instance of 20 in a program to change it to the new department number value, you might inadvertently change the value of one instance of 20 that is being used for something else, such as a payroll deduction value.
-   Using named constants reduces typographical errors. For example, if you must include 20 at several places within a program, you might inadvertently type 10 or 200 for one of the instances, and the compiler will not recognize the mistake. However, if you use the identifier NUMBER_OF_DEPTS, the compiler will ensure that you spell it correctly.
-   When you use a named constant in an expression, it stands out as different from a variable. For example, in the following arithmetic statement, it is easy to see which elements are variable and which are constant because the constants have been named conventionally using all uppercase letters and underscore to separate words:

double payAmount = hoursWorked * STD_PAY_RATE – numDependents * DEDUCTION;

Although many programmers use named constants to stand for most of the constant values in their programs, many make an exception when using 0 or 1.

**The Scope of Variables and Constants**
A data item’s scope is the area in which it is visible to a program and in which you can refer to it using its simple identifier. A variable or constant is in scope from the point it is declared until the end of the block of code in which the declaration lies. A block of code is the code contained between a set of curly braces. So, if you declare a variable or constant within a method, it can be used from its declaration until the end of the method unless the method contains multiple sets of curly braces. Then, a data item is usable only until the end of the block that holds the declaration.