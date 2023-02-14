---
aliases:
tags:
---
**[[COMPROG12LEC|MAINHUB]]**

---
## Creating Methods that Return Values
A method ends when any of the following events takes place:
-   The method completes all of its statements. You have seen methods like this in the last section.
-   The method throws an exception. Exceptions are errors; you will learn about them in the chapter “Exception Handling.”
-   The method reaches a return statement. A return statement causes a method to end and the program’s logic to return to the calling method. Also, a return statement frequently sends a value back to the calling method.

The return type for a method can be any type used in Java, which includes the primitive types `int`, `double`, `char`, and so on, as well as class types (including class types you create). Of course, a method can also return nothing, in which case the return type is void.

A method’s return type is known more succinctly as a method’s type. For example, the declaration for the `displayAddress()` method shown earlier in Figure 3-4 is written as follows:

`public static void displayAddress()`
This method returns no value, so it is type void.

A method that prompts a user for an age and returns the age to the calling method might be declared as:

`public static int getAge()`
The method returns an int, so it is type `int`.

As another example, a method that returns true or false depending on whether an employee worked overtime hours might be declared as:

`public static boolean workedOvertime()`
This method returns a Boolean value, so it is type `boolean`.

The `predictRaise()` method shown earlier produces output, but does not return any value, so its return type is void. If you want to create a method to return the new, calculated salary value rather than display it, the header would be written as follows:

`public static double predictRaise(double salary)`

Figure 3-19 shows this method.
![[COMPROG12LECPRELIMch34image0.png|center]]