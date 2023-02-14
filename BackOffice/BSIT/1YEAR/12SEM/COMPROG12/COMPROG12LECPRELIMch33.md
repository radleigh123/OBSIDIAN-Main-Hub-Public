---
aliases:
tags:
---
**[[COMPROG12LEC|MAINHUB]]**

---
## Adding Parameters to Methods
Some methods require that data be sent to them when they are called. Data items you use in a call to a method are called arguments. When the method receives the data items, they are called parameters. Methods that receive data are flexible because they can produce different results depending on what data they receive.

As a real-life example, when you make a restaurant reservation, you do not need to employ a different method for every date of the year at every possible time of day. Rather, you can supply the date and time as information to the person who carries out the method. The method, recording the reservation, is then carried out in the same manner, no matter what date and time are supplied.

In a program, if you design a method to square numeric values, it makes sense to design a `square()` method that you can supply with an argument that represents the value to be squared, rather than having to develop a square1() method (that squares the value 1), a `square2()` method (that squares the value 2), and so on. To call a `square()` method that takes an argument, you might write a statement like `square(17)`; or `square(86)`;. Similarly, any time it is called, the `println()` method can receive any one of an infinite number of arguments—for example, “Hello”, “Goodbye”, or any other String. No matter what message is sent to `println()`, the message is displayed correctly. If the `println()` method could not accept arguments, it would not be practical to use.

In everyday life, you use many methods without understanding how they work. For example, when you make a real-life restaurant reservation, you do not need to know how the reservation is actually recorded at the restaurant—perhaps it is written in a book, marked on a large chalkboard, or entered into a computerized database. The implementation details don’t concern you as a client, and if the restaurant changes its methods from one year to the next, the change does not affect your use of the reservation method—you still call and provide your name, a date, and a time.

Similarly, object-oriented programs use implementation hiding, which describes the encapsulation of method details. It means that a client does not have to know how a method works internally, but only needs to know the name of the called method and what type of information to send. (Usually, you also want to know about any data returned by the method; you will learn about returned data later in this chapter.) In other words, the calling method needs to understand only the interface to the called method. The interface is the only part of a method that the method’s client sees or with which it interacts. In addition, if you substitute a new or revised method implementation, as long as the interface to the method does not change, you won’t need to make any changes in any methods that call the altered method.

**Creating a Method that Receives a Single Parameter**
When a method can receive a parameter, its declaration contains the same elements as one that does not accept a parameter—optional access specifiers, the return type for the method, the method name, and a set of parentheses that include two items:
-   The parameter type
-   A local name for the parameter

For example, the declaration for a public method named `predictRaise()` that accepts a person’s annual salary and computes the value of a 10 percent raise could be written as follows:
`public static void predictRaise(double salary)`

You can think of the parentheses in a method declaration as a funnel into the method— parameters listed there contain data that is “dropped into” the method. A parameter accepted by a method can be any data type, including the primitive types, such as `int`, `double`, and `char`; it also can be a built-in class type such as `String` or `PrintStream`, or a class type you create.

In the method header for `predictRaise()`, the parameter double salary within the parentheses indicates that the method will receive a value of type `double`, and that within the method, the passed value will be known as salary. Figure 3-13 shows a complete method.

![[COMPROG12LECPRELIMch33image0.png|center]]

The `predictRaise()` method is a void method because it does not need to return a value to any other method that calls it—its only function is to receive the salary value, multiply it by the **RAISE_RATE** constant (1.10, which results in a 10 percent salary increase), and then display the result.

The `predictRaise()` method’s parameter is a double, so you call it using any argument that can be promoted to a double. In other words, because `predictRaise()` accepts a double, it can also accept a `float`, `long`, `int`, `short`, or `byte`. (See Figure 2-41 in Chapter 2 to review the order for establishing unifying data types.) The argument can be a constant, variable, or more complicated expression.

It is interesting to note that if the value used as an argument in the method call to `predictRaise()` is a variable, it might possess the same identifier as salary or a different one, such as `startingWage`. For example, the code in Figure 3-14 shows three calls to the `predictRaise()` method, and Figure 3-15 shows the output. One call uses a constant, 400.00. The other two use variables—one with the same name as salary and the other with a different name, `startingWage`. The identifier salary in the main() method refers to a different memory location than the one in the `predictRaise()` method. The parameter salary is simply a placeholder while it is being used within the `predictRaise()` method, no matter what name its value “goes by” in the calling method. The parameter salary is a local variable to the `predictRaise()` method; that is, it is known only within the boundaries of the method. The variable and constant declared within the method are also local to the method.

![[COMPROG12LECPRELIMch33image1.png|center]]

Each time the `predictRaise()` method in Figure 3-14 executes, a salary variable is redeclared—that is, a new memory location large enough to hold a double is set up and named salary. Within the `predictRaise()` method, salary holds a copy of whatever value is passed into the method by the main() method. When the `predictRaise()` method ends at the closing curly brace, the local salary variable ceases to exist. That is, if you change the value of salary after you have used it in the calculation within `predictRaise()`, it affects nothing else. The memory location that holds salary is released at the end of the method, and any changes to its value within the method do not affect any value in the calling method. In particular, don’t think there would be any change in the variable named salary in the main() method; that variable, even though it has the same name as the locally declared parameter in the `predictRaise()` method, is a different variable with its own memory address.

**Creating a Method that Requires Multiple Parameters**
A method can require more than one parameter. For example, rather than creating a `predictRaise()` method that adds a 10 percent raise to every person’s salary, you might prefer to create a method to which you can pass two values—the salary to be raised as well as a percentage figure by which to raise it. Figure 3-16 shows a method that uses two such parameters.

![[COMPROG12LECPRELIMch33image2.png|center]]

In Figure 3-16, two parameters (double salary and double rate) appear within the parentheses in the method header. A comma separates each parameter, and each parameter requires its own declared type (in this case, both are double) as well as its own identifier. Note that a declaration for a method that receives two or more parameters must list the type for each parameter separately, even if the parameters have the same type.

You can pass multiple arguments to a method by listing the arguments within the call to the method and separating them with commas. When values are passed to the method in a statement such as the following, the first value passed is referenced as salary within the method, and the second value passed is referenced as rate:
`predictRaiseUsingRate(mySalary, promisedRate);`

Arguments to a method must be passed in the correct order. The call `predictRaiseUsingRate(200.00, 0.10);` results in output representing a 10 percent raise based on a $200.00 salary amount (or $220.00), but `predictRaiseUsingRate(0.10, 200.00);` results in output representing a 20,000 percent raise based on a salary of 10 cents (or $20.10).

If arguments to a method are passed in the wrong order, the result is one of the following:
-   If the method can still accept both arguments, the result is a logical error; that is, the program compiles and executes, but it probably produces incorrect results.
-   If the method cannot accept the arguments, passing arguments in the wrong order constitutes a syntax error, and the program does not compile.

You can write a method so that it takes any number of parameters in any order. However, when you call a method, the arguments you send to a method must match in order—both in number and in type—the parameters listed in the method declaration. A method’s signature is the combination of the method name and the number, types, and order of arguments. A method call must match the called method’s signature.

Thus, a method to compute an automobile salesperson’s commission amount might require arguments such as an integer dollar value of a car sold, a double percentage commission rate, and a character code for the vehicle type. The correct method executes only when three arguments of the correct types are sent in the correct order. Figure 3-17 shows a class containing a three-parameter method and a main() method that calls it twice, once using variable arguments and again using constant arguments. Figure 3-18 shows the output of the application.

![[COMPROG12LECPRELIMch33image3.png|center]]