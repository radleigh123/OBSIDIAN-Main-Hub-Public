---
aliases:
tags:
---
**[[COMPROG12LEC|MAINHUB]]**

---
## Overloading a Method
Overloading a method allows you to use one identifier to execute diverse tasks. In Java, it more specifically means writing multiple methods in the same scope that have the same name but different parameter lists. In overloaded methods, the parameter identifiers do not have to be different, but the parameter lists must satisfy one or both of these conditions:
-   The lists must have different numbers of parameters. For example, one list could have one double, another list could have two doubles, and a third list could have 10 doubles.
-   The lists must have parameter data types in different orders. For example, one list could have two doubles, another could have an `int` and a `double`, and a third could have a double and an int.

When you use the English language, you overload words all the time. When you say “open the door,” “open your eyes,” and “open a computer file,” you are talking about three very different actions using very different methods and producing very different results. However, anyone who speaks English fluently has no trouble understanding your meaning because the verb open is understood in the context of the noun that follows it.

When you overload a Java method, multiple methods share a name, and the compiler understands which one to use based on the arguments in the method call. For example, suppose you create a class method to apply a simple interest rate to a bank balance. The method is named `calculateInterest();` it receives two double parameters—the balance and the interest rate—and displays the multiplied result. Figure 4-12 shows the method.

![[COMPROG12LECPRELIMch35image0.png|center]]

When an application calls the `calculateInterest()` method and passes two double values, as in `calculateInterest(1000.00, 0.04)`, the interest is calculated correctly as 4% of $1000.00. 

Assume, however, that different users want to calculate interest using different argument types. Some users who want to indicate an interest rate of 4% might use 0.04; others might use 4 and assume that it means 4%. When the `calculateInterest()` method is called with the arguments 1000.00 and 0.04, the interest is calculated correctly as 40.00. When the method is called using 1000.00 and 4, the method works because the integer argument is promoted to a double, but the interest is calculated incorrectly as 4000.00, which is 100 times too high.

A solution for the conflicting use of numbers to represent parameter values is to overload the `calculateInterest()` method. For example, in addition to the `calculateInterest()` method shown in Figure 4-12, you could add the method shown in Figure 4-13.

![[COMPROG12LECPRELIMch35image1.png|center]]

If an application calls the method `calculateInterest()` using two double arguments—for example, `calculateInterest(1000.00, 0.04)`—the first version of the method, the one shown in Figure 4-12, executes. However, if an integer is used as the second argument in a call to `calculateInterest()`—as in `calculateInterest(1000.00, 4)`—the second version of the method, the one shown in Figure 4-13, executes. In this second example, the whole number rate figure is correctly divided by 100.0 before it is used to determine the interest earned. 

Of course, you could use methods with different names to solve the dilemma of producing an accurate interest figure—for example, `calculateInterestUsingDouble()` and `calculateInterestUsingInt()`. However, it is easier and more convenient for programmers who use your methods to remember just one method name they can use in the form that is most appropriate for their programs. It is convenient to be able to use one reasonable name for tasks that are functionally identical except for the argument types that can be passed to them. The compiler knows which method version to call based on the passed arguments.

**Automatic Type Promotion in Method Calls**
You learned that Java casts variables to a unifying type when you perform arithmetic with unlike types. For example, when you multiply an `int` and a `double`, the result is a double. In a similar way, Java can promote one data type to another when you pass a parameter to a method. For example, if a method has a double parameter and you pass in an integer, the integer is promoted to a double. Recall that the order of promotion is double, float, long, and int. Any type in this list can be promoted to any type that precedes it.

When an application contains just one version of a method, you can call the method using a parameter of the correct data type or one that can be promoted to the correct data type. For example, consider the simple method shown in Figure 4-14.

![[COMPROG12LECPRELIMch35image2.png|center]]

If you write an application in which you declare `doubleValue` as a double variable and `intValue` as an int variable (as shown in Figure 4-15), either of the two method calls `simpleMethod(doubleValue);` or `simpleMethod(intValue);` results in the output “*Method receives double parameter*”. The call that uses the integer works because the integer is cast as (or promoted to) a double. The output of the program in Figure 4-15 is shown in Figure 4-16.

![[COMPROG12LECPRELIMch35image3.png|center]]

![[COMPROG12LECPRELIMch35image4.png|center]]

Note that if the method with the declaration `void simpleMethod(double d)` did not exist, but the declaration `void simpleMethod(int i)` did exist, then the method call simpleMethod(doubleValue); would fail. Although an `int` can be promoted to a `double`, a double is not automatically reduced to an int. This makes sense if you consider the potential loss of information when a double value is reduced to an integer.

Suppose that you add an overloaded version of `simpleMethod()` to the program in Figure 4-15. This version accepts an integer parameter, as shown in Figure 4-17. When you properly overload a method, you can call it providing different argument lists, and the appropriate version of the method executes. Now, the output changes when you call `simpleMethod(intValue);`. Instead of promoting an integer argument to a double, the compiler recognizes a more exact match for the method call that uses the integer argument, so it calls the version of the method that produces the output “*Method receives integer parameter*”. Figure 4-18 shows the output.

![[COMPROG12LECPRELIMch35image5.png|center]]

![[COMPROG12LECPRELIMch35image6.png|center]]