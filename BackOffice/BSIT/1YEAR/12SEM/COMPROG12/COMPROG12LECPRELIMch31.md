---
aliases:
tags:
---
**[[COMPROG12LEC|MAINHUB]]**

---
## Understanding Method Calls and Placement
A method is a program module that contains a series of statements that carry out a task. You have already seen Java classes that contain a `main()` method, which executes automatically when you run a program. A program’s `main()` method can execute additional methods, and those methods can execute others. Any class can contain an unlimited number of methods, and each method can be called an unlimited number of times.

To execute a method, you invoke or call it. In other words, a calling method makes a method call, and the method call invokes a called method. The calling method is also known as a client method because a called method provides a service for its client. 

Consider the simple First class that you saw in Chapter 1; it displayed a single line of output, “First Java application.” Suppose that you want to add three lines of output to this application to display your company’s name and address. One approach would be to simply add three new `println()` statements, as shown in the shaded statements in Figure 3-1.

![[COMPROG12LECPRELIMch31image0.png|center]]

Instead of adding the three `println()` statements to the application in Figure 3-1, you might prefer to call a method that executes the three statements. Then the program would look like the one in Figure 3-2. The shaded line contains the call to the `displayAddress()` method.

![[COMPROG12LECPRELIMch31image1.png|center]]

There are two major advantages to creating a separate method to display the three address lines. First, the `main()` method remains short and easy to follow because `main()` contains just one statement to call the method, rather than three separate `println()` statements to perform the work of the method. What is more important is that a method is easily reusable. After you create the `displayAddress()` method, you can use it in any application that needs the company’s name and address. In other words, you do the work once, and then you can use the method many times. In the following examples, a method is called from another method in its own class; later in this chapter, you learn how to call a method from a different class.

Besides adding a call to the method in the First class, you must actually write the method. You place a method within a class, but it must be outside of any other methods. In other words, you cannot place a method within another method. Figure 3-3 shows the two locations where you can place additional methods within the First class—within the curly braces of the class, but outside of (either before or after) any other methods. Methods can never overlap.

![[COMPROG12LECPRELIMch31image2.png|center]]

The order in which methods appear in a class has no bearing on the order in which the methods are called or executed. No matter where you place it, the `main()` method is always executed first in any Java application, and it might call any other methods in any order and any number of times. The order in which you call methods, not their physical placement, is what makes a difference in how an application executes.

A `main()` method executes automatically when you run a program, but other methods do not execute simply because you place them within a class—they must be called. A class might contain methods that are never called from a particular application, just as some electronic devices might contain features you never use. For example, you might use a DVR to play movies but never to record TV programs, or you might use your microwave oven for popcorn but never to defrost.

Figure 3-4 shows the First class with two methods: the main() method and the `displayAddress()` method placed after main(). Figure 3-5 shows the output from the execution of the First class in Figure 3-4. When the program executes, the `main()` method first calls the `displayAddress()` method, which displays three lines of output. Then `main()` displays the phrase “First Java application”.

![[COMPROG12LECPRELIMch31image3.png|center]]