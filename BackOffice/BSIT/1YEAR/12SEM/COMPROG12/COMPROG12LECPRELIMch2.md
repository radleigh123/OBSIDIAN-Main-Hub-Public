---
aliases:
tags:
---
**[[COMPROG12LEC|BACK]]**

---
## Comparing Procedural and Object-Oriented Programming Concepts
Two popular approaches to writing computer programs are procedural programming and object-oriented programming.

**Procedural Programming**
Procedural programming is a style of programming in which operations are executed one after another in sequence. In procedural applications, you create names for computer memory locations that can hold values—for example, numbers and text—in electronic form. The named computer memory locations are called variables because they hold values that might vary. For example, a payroll program might contain a variable named rateOfPay. The memory location referenced by the name rateOfPay might contain different values (a different value for every employee of the company) at different times. During the execution of the payroll program, each value stored under the name rateOfPay might have many operations performed on it—for example, the value might be read from an input device, be multiplied by another variable representing hours worked, and be printed on paper.

For convenience, the individual operations used in a computer program are often grouped into logical units called procedures. For example, a series of four or five comparisons and calculations that together determine a person’s federal withholding tax value might be grouped as a procedure named calculateFederalWithholding. A procedural program defines the variable memory locations and then calls a series of procedures to input, manipulate, and output the values stored in those locations. When a program calls a procedure, the current logic is temporarily abandoned so that the procedure’s commands can execute. A single procedural program often contains hundreds of variables and procedure calls. Procedures are also called modules, methods, functions, and subroutines. Users of different programming languages tend to use different terms.

**Object-Oriented Programming**
Object-oriented programming is an extension of procedural programming in which you take a slightly different approach to writing computer programs. Writing object-oriented programs involves:
-   Creating classes, which are blueprints for objects
-   Creating objects, which are specific instances of those classes
-   Creating applications that manipulate or use those objects

Originally, object-oriented programming was used most frequently for two major types of applications:

**Computer simulations**, which attempt to mimic real-world activities so that their processes can be improved or so that users can better understand how the real-world processes operate

**Graphical user interfaces**, or GUIs (pronounced “gooeys”), which allow users to interact with a program in a graphical environment.

Thinking about objects in these two types of applications makes sense. For example, a city might want to develop a program that simulates traffic patterns to help prevent traffic tie-ups. Programmers would create classes for objects such as cars and pedestrians that contain their own data and rules for behavior. For example, each car has a speed and a method for changing that speed. The specific instances of cars could be set in motion to create a simulation of a real city at rush hour.

Creating a GUI environment for users is also a natural use for object orientation. It is easy to think of the components a user manipulates on a computer screen, such as buttons and scroll bars, as similar to real-world objects. Each GUI object contains data—for example, a button on a screen has a specific size and color. Each object also contains behaviors—for example, each button can be clicked and reacts in a specific way when clicked. Some people consider the term object-oriented programming to be synonymous with GUI programming, but object-oriented programming means more. Although many GUI programs are object-oriented, not all object-oriented programs use GUI objects. Modern businesses use object-oriented design techniques when developing all sorts of business applications, whether they are GUI applications or not. 

Understanding object-oriented programming requires grasping three basic concepts:
-   Encapsulation as it applies to classes as objects
-   Inheritance
-   Polymorphism

**Understanding Classes, Objects, and Encapsulation**  
In object-oriented terminology, a class is a term that describes a group or collection of objects with common properties. In the same way that a blueprint exists before any houses are built from it, and a recipe exists before any cookies are baked from it, a class definition exists before any objects are created from it. A class definition describes what attributes its objects will have and what those objects will be able to do. Attributes are the characteristics that define an object; they are properties of the object. When you learn a programming language such as Java, you learn to work with two types of classes: those that have already been developed by the language’s creators and your own new, customized classes.

An object is a specific, concrete instance of a class. Creating an instance is called instantiation. You can create objects from classes that you write and from classes written by other programmers, including Java’s creators. The values contained in an object’s properties often differentiate instances of the same class from one another. For example, the class Automobile describes what Automobile objects are like. Some properties of the Automobile class are make, model, year, and color. Each Automobile object possesses the same attributes, but not necessarily the same values for those attributes. One Automobile might be a 2010 white Ford Taurus and another might be a 2015 red Chevrolet Camaro. Similarly, your dog has the properties of all Dogs, including a breed, name, age, and whether its shots are current. The values of the properties of an object are referred to as the object’s state. In other words, you can think of objects as roughly equivalent to nouns, and of their attributes as similar to adjectives that describe the nouns.

When you understand an object’s class, you understand the characteristics of the object. If your friend purchases an Automobile, you know it has a model name, and if your friend gets a Dog, you know the dog has a breed. Knowing what attributes exist for classes allows you to ask appropriate questions about the states or values of those attributes. For example, you might ask how many miles the car gets per gallon, but you would not ask whether the car has had shots. Similarly, in a GUI operating environment, you expect each component to have specific, consistent attributes and methods, such as a window having a title bar and a close button, because each component gains these properties as a member of the general class of GUI components. Figure 1-2 shows the relationship of some Dog objects to the Dog class.

![[COMPROG12LECPRELIMch2image0.png|center wm-sm]]

Besides defining properties, classes define methods their objects can use. A method is a self-contained block of program code that carries out some action, similar to a procedure in a procedural program. An Automobile, for example, might have methods for moving forward, moving backward, and determining the status of its gas tank. Similarly, a Dog might have methods for walking, eating, and determining its name, and a program’s GUI components might have methods for maximizing and minimizing them as well as determining their size. In other words, if objects are similar to nouns, then methods are similar to verbs. 

In object-oriented classes, attributes and methods are encapsulated into objects.

Encapsulation refers to two closely related object-oriented notions:
-   Encapsulation is the enclosure of data and methods within an object. Encapsulation allows you to treat all of an object’s methods and data as a single entity. Just as an actual dog contains all of its attributes and abilities, so would a program’s Dog object.
-   Encapsulation also refers to the concealment of an object’s data and methods from outside sources. Concealing data is sometimes called information hiding, and concealing how methods work is implementation hiding; you will learn more about both terms in the lesson “Using Methods, Classes, and Objects.” Encapsulation lets you hide specific object attributes and methods from outside sources and provides the security that keeps data and methods safe from inadvertent changes.

If an object’s methods are well written, the user can be unaware of the low-level details of how the methods are executed, and the user must simply understand the interface or interaction between the method and the object. For example, if you can fill your Automobile with gasoline, it is because you understand the interface between the gas pump nozzle and the vehicle’s gas tank opening. You don’t need to understand how the pump works mechanically or where the gas tank is located inside your vehicle. If you can read your speedometer, it does not matter how the displayed figure is calculated. As a matter of fact, if someone produces a superior, more accurate speed-determining device and inserts it in your Automobile, you don’t have to know or care how it operates, as long as your interface remains the same. The same principles apply to well-constructed classes used in object-oriented programs—programs that use classes only need to work with interfaces.

**Understanding Inheritance and Polymorphism**
An important feature of object-oriented program design is inheritance—the ability to create classes that share the attributes and methods of existing classes, but with more specific features. For example, Automobile is a class, and all Automobile objects share many traits and abilities. Convertible is a class that inherits from the Automobile class; a Convertible is a type of Automobile that has and can do everything a “plain” Automobile does—but with an added ability to lower its top. (In turn, Automobile inherits from the Vehicle class.) Convertible is not an object—it is a class. A specific Convertible is an object—for example, my1967BlueMustangConvertible.

Inheritance helps you understand real-world objects. For example, the first time you encounter a convertible, you already understand how the ignition, brakes, door locks, and other systems work because you realize that a convertible is a type of automobile, so you need to be concerned only with the attributes and methods that are “new” with a convertible. The advantages in programming are the same—you can build new classes based on existing classes and concentrate on the specialized features you are adding.

A final important concept in object-oriented terminology is polymorphism. Literally, polymorphism means “many forms”—it describes the feature of languages that allows the same word or symbol to be interpreted correctly in different situations based on the context. For example, although the classes Automobile, Sailboat, and Airplane all inherit from Vehicle, turn and stop methods work differently for instances of those classes. The advantages of polymorphism will become more apparent when you begin to create GUI applications containing features such as windows, buttons, and menu bars. In a GUI application, it is convenient to remember one method name, such as `setColor` or `setHeight`, and have it work correctly no matter what type of object you are modifying. When you see a plus sign (+) between two numbers, you understand they are being added.

When you see it carved in a tree between two names, you understand that the names are linked romantically. Because the symbol has diverse meanings based on context, it is polymorphic.