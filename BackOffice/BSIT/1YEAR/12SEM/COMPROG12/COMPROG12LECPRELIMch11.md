---
aliases:
tags:
---
**[[COMPROG12LEC|BACK]]**

---
## Learning Programming Terminology
A **computer program** is a set of instructions that you write to tell a computer what to do. Computer equipment, such as a monitor or keyboard, is hardware, and programs are software. A program that performs a task for a user (such as calculating and producing paychecks, word processing, or playing a game) is **application software**; a program that manages the computer itself (such as Windows or Linux) is **system software**. The logic behind any computer program, whether it is an application or system program, determines the exact order of instructions needed to produce desired results.

All computer programs ultimately are converted to machine language. **Machine language**, or *machine code*, is the most basic set of instructions that a computer can execute. Each type of processor (the internal hardware that handles computer instructions) has its own set of machine language instructions. Programmers often describe machine language using 1s and 0s to represent the on-and-off circuitry of computer systems.

The system that uses only 1s and 0s is the **binary numbering system**. Later in this chapter, you will learn that **bytecode** is the name for the binary code created when Java programs are converted to machine language.

***Machine language*** is a low-level programming language, or one that corresponds closely to a computer processor’s circuitry. *Low-level languages* require you to use memory addresses for specific machines when you create commands. This means that low-level languages are difficult to use and must be customized for every type of machine on which a program runs.

Fortunately, programming has evolved into an easier task because of the development of high-level programming languages. A *high-level programming language* allows you to use a vocabulary of reasonable terms, such as read, write, or add, instead of the sequences of 1s and 0s that perform these tasks. High-level languages also allow you to assign single-word, intuitive names to areas of computer memory where you store data. This means you can use identifiers such as hoursWorked or rateOfPay, rather than having to remember their memory locations. Currently, over 2,000 high-level programming languages are available to developers; Java is one of them.

Each high-level language has its own syntax, or rules about how language elements are combined correctly to produce usable statements. For example, depending on the specific high-level language, you might use the verb print or write to produce output. All languages have a specific, limited vocabulary (the language’s keywords) and a specific set of rules for using that vocabulary. When you are learning a computer programming language, such as Java, C++, or Visual Basic, you really are learning the vocabulary and syntax for that language.

Using a programming language, programmers write a series of program statements, similar to English sentences, to carry out the tasks they want the program to perform. Program statements are also known as commands because they are orders to the computer, such as “output this word” or “add these two numbers.”

After the program statements are written, high-level language programmers use a computer program called a compiler or interpreter to translate their language statements into machine language. A **compiler** translates an entire program before carrying out any statements, or executing them, whereas an **interpreter** translates one program statement at a time, executing a statement as soon as it is translated.

Whether you use a compiler or interpreter often depends on the programming language you use. For example, <mark class="hltr-blue">C++ is a compiled language</mark>, and <mark class="hltr-blue">Visual Basic is an interpreted language</mark>. Each type of translator has its supporters; programs written in compiled languages execute more quickly, whereas programs written in interpreted languages can be easier to develop and debug. Java uses the best of both technologies: a compiler to translate your programming statements and an interpreter to read the compiled code line by line when the program executes (also called at **run time**).

Compilers and interpreters issue one or more error messages each time they encounter an invalid program statement—that is, a statement containing a **syntax error**, or misuse of the language. Examples of syntax errors include misspelling a keyword or omitting a word that a statement requires. When a syntax error is detected, the programmer can correct the error and attempt another translation. Repairing all syntax errors is the first part of the process of **debugging** a program—freeing the program of all flaws or errors, also known as bugs.