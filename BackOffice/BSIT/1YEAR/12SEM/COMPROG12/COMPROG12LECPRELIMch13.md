---
aliases:
tags:
---
**[[COMPROG12LEC|BACK]]**

---
## Analyzing a Java Application that produces console output
At first glance, even the simplest Java application involves a fair amount of confusing syntax.

Consider the application in Figure 1-4. This program is written on seven lines, and its only task is to display “First Java application” on the screen.

![[COMPROG12LECPRELIMch3image0.png|center wm-sm]]

**Understanding the Statement that Produces the Output**
Although the program in Figure 1-4 occupies several lines, it contains only one Java programming statement. The statement System.out.println("First Java application"); does the actual work in this program. Like all Java statements, this one ends with a semicolon. Most Java programming statements can be spread across as many lines as you choose, as long as you place line breaks in appropriate places. For example, in the program in Figure 1-4, you could place a line break before or after the opening parenthesis, or before or after the closing parenthesis. However, you usually want to place a short statement on a single line. 

The text “First Java application” is a literal string of characters—a series of characters that will appear in output exactly as entered. Any literal string in Java is written between double quotation marks. In Java, a literal string cannot be broken and placed on multiple lines. Figure 1-5 labels this string and the other parts of the statement.

![[COMPROG12LECPRELIMch3image1.png|center wm-tl]]

The string “First Java application” appears within parentheses because the string is an argument to a method, and arguments to methods always appear within parentheses. Arguments are pieces of information that are sent into a method. The act of sending arguments to a method is called passing arguments to the method. As an analogy, consider placing a catalog order with a company that sells sporting goods. Processing a catalog order is a method that consists of a set of standard procedures—recording the order, checking the availability of the item, pulling the item from the warehouse, and so on. Each catalog order also requires a set of data items, such as which item number you are ordering and the quantity of the item desired; these data items can be considered the arguments to the order-processing method. If you order two of item 5432 from a catalog, you expect different results than if you order 1,000 of item 9008. Likewise, if you pass the argument “Happy Holidays” to a Java display method, you expect different results than if you pass the argument “First Java application”.

**Understanding the First Class**
Everything that you use within a Java program must be part of a class. When you write public class First, you are defining a class named First. You can define a Java class using any name or identifier you need, as long as it meets the following requirements:
-   A Java identifier must begin with a letter of the English alphabet, a non-English letter (such as αα or ΠΠ), an underscore, or a dollar sign. A class name cannot begin with a digit.
-   A Java identifier can contain only letters, digits, underscores, or dollar signs.
-   A Java identifier cannot be a reserved keyword, such as public or class. (See Table 1-1 for a list of reserved keywords.)
-   A Java identifier cannot be one of the following values: true, false, or null. These are not keywords (they are primitive values), but they are reserved and cannot be used. ![[COMPROG12LECPRELIMch3image2.png|wm-tl]]

It is a Java standard, although not a requirement, to begin class identifiers with an uppercase letter and employ other uppercase letters as needed to improve readability. (By contrast, method identifiers, like println(), conventionally begin with a lowercase letter.) The style that joins words in which each word begins with an uppercase letter is called Pascal casing, or sometimes upper camel casing. You should follow established conventions for Java so your programs will be easy for other programmers to interpret and follow. This book uses established Java programming conventions.

Table 1-2 lists some valid and conventional class names that you could use when writing programs in Java. Table 1-3 provides some examples of class names that could be used in Java (if you use these class names, the class will compile) but that are unconventional and not recommended. Table 1-4 provides some class name examples that are illegal.

![[COMPROG12LECPRELIMch3image3.png|center wm-tl]]

In Figure 1-4 (and again in Figure 1-6), the line public class First is the class header; it contains the keyword class, which identifies First as a class. The reserved word public is an access specifier. An access specifier defines the circumstances under which a class can be accessed and the other classes that have the right to use a class. Public access is the most liberal type of access; you will learn about public access and other types of access in the chapter “Using Methods, Classes, and Objects.”

![[COMPROG12LECPRELIMch3image4.png|center wm-sm]]

After the class header, you enclose the contents of a class within curly braces ({ and }); any data items and methods between the curly braces make up the class body. A class body can be composed of any number of data items and methods. In Figure 1-4 (and again in Figure 1-6), the class First contains only one method within its curly braces. The name of the method is main(), and the main() method, like the println() method, includes its own set of parentheses. The main() method in the First class contains only one statement—the statement that uses the println() method. The main() method does not contain any other methods, but it calls the println() method.

**Indent Style**
In general, whitespace is optional in Java. Whitespace is any combination of nonprinting characters. You use whitespace to organize your program code and make it easier to read.

You can insert whitespace between words or lines in your program code by typing spaces, tabs, or blank lines because the compiler ignores these extra spaces. However, you cannot use whitespace within an identifier or keyword, or surrounding the dots in any class-object method combination.

For every opening curly brace ({) in a Java program, there must be a corresponding closing curly brace (}), but the placement of the opening and closing curly braces is not important to the compiler. For example, the following class executes in exactly the same way as the one shown in Figure 1-4. The only difference is the layout of the braces—the line breaks occur in different locations.

![[COMPROG12LECPRELIMch3image5.png]]

The indent style shown in the preceding example, in which opening braces do not stand alone on separate lines, is known as the K & R style and is named for Kernighan and Ritchie, who wrote the first book on the C programming language.

**Understanding the main() Method**
The method header for the main() method is quite complex. Figure 1-7 shows the parts of the main() method.

![[COMPROG12LECPRELIMch3image6.png]]

The meaning and purpose of each of the terms used in the method header will become clearer as you complete this textbook; a brief explanation will suffice for now.
-   In the method header public static void main(String[] args), the word public is an access specifier, just as it is when you use it to define the First class.
-   In Java, the reserved keyword static means that a method is accessible and usable even though no objects of the class exist.
-   The keyword void used in the main() method header indicates that the main() method does not return any value when it is called. This doesn’t mean that main() doesn’t produce output—in fact, the method in Figure 1-4 (and in Figure 1-7) does. It only means that the main() method does not send any value back to any other method that might use it. You will learn more about return values in the chapter “Methods, Classes, and Objects.”
-   The name of the method is main(). As is the convention with Java methods, its identifier begins with a lowercase letter. Not all classes have a main() method; in fact, many do not. All Java applications, however, must include a class containing a public method named main(), and most Java applications have additional classes and methods. When you execute a Java application, the JVM always executes the main() method first.
-   In the method header public static void main(String[] args), the contents between the parentheses, String[] args, represent the type of argument that can be passed to the main() method, just as the string "First Java application" is an argument passed to the println() method. String is a Java class that can be used to hold character strings (according to Java convention, it begins with an uppercase letter, like other classes). The identifier args is used to hold any String objects that might be sent to the main() method. The main() method could do something with those arguments, such as display them, but in Figure 1-4, the main() method does not actually use the args identifier. Nevertheless, you must place an identifier within the main() method’s parentheses. The identifier does not need to be named args—it could be any legal Java identifier—but the name args is traditional.