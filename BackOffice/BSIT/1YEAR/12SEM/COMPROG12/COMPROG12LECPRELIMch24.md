---
aliases:
tags:
---
**[[COMPROG12LEC|BACK]]**

---
## Using the Scanner Class to accept keyboard input
Although you can assign values to variables you declare, programs typically become more useful when a user can supply different values for variables each time a program executes. In Chapter 1, you learned how to display output on the monitor using the System.out property. System.out refers to the standard output device, which usually is the monitor. To create interactive programs that accept input from a user, you can use System.in, which refers to the standard input device (normally the keyboard).

You have learned that you can use the print() and println() methods to display many data types; for example, you can use them to display a double, int, or String. The System.in object is not as flexible; it is designed to read only bytes. That’s a problem, because you often want to accept data of other types. Fortunately, the designers of Java have created a class named Scanner that makes System.in more flexible.

To create a Scanner object and connect it to the System.in object, you write a statement similar to the following:

_Scanner inputDevice = new Scanner(System.in);_

The portion of the statement to the left of the assignment operator, Scanner inputDevice, declares an object of type Scanner with the programmer-chosen name inputDevice, in exactly the same way that int x; declares an integer with the programmer-chosen name x.

The portion of the statement to the right of the assignment operator, new Scanner(System.in), creates a Scanner object that is connected to the System.in property. In other words, the created Scanner object is connected to the default input device. The keyword new is required by Java; you will use it whenever you create objects that are more complex than the primitive data types.

The assignment operator in the Scanner declaration statement assigns the value of the new object—that is, its memory address—to the inputDevice object in the program. 

The Scanner class contains methods that retrieve values from an input device. Each retrieved value is a token, which is a set of characters that is separated from the next set by whitespace. Most often, this means that data is accepted when a user presses the Enter key, but it could also mean that a token is accepted after a space or tab. Table 2-7 summarizes some of the most useful methods that read different data types from the default input device. Each retrieves a value from the keyboard and returns it if the next token is the correct data type.

![[COMPROG12LECPRELIMch24image0.png|center wm-tl]]

Figure 2-17 contains a program that uses two of the Scanner class methods. The program reads a string and an integer from the keyboard and displays them. The Scanner class is used in the four shaded statements in the figure.
-   The first shaded statement imports the package necessary to use the Scanner class.
-   The second shaded statement declares a Scanner object named inputDevice.
-   The third shaded statement uses the nextLine() method to retrieve a line of text from the keyboard and store it in the name variable.
-   The last shaded statement uses the nextInt() method to retrieve an integer from the keyboard and store it in the age variable.

![[COMPROG12LECPRELIMch24image1.png|center wm-tl]]