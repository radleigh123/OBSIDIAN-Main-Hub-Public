**PasteBin**
**Github Gist**

From just starting main focus to use is:
- Cloud computing (*IaaS*, *PaaS*, *SaaS*)
- Backend Programming ➡ Backend Framework (*ExpressJS*, *django*, *Java Spring*)
- Primary Database (*MySQL*, *PostreSQL*, *MongoDB*)

### Programming
- **OpenClassrooms** (*Free Programming Course*)
- [Memory management in C: The heap and the stack](https://web.archive.org/web/20170829060314/http://www.inf.udec.cl/~leo/teoX.pdf)
- [Building multiple cpp files](https://stackoverflow.com/questions/47665886/vs-code-will-not-build-c-programs-with-multiple-ccp-source-files)
- [Online CPP Compiler](https://cppinsights.io/)
- **[[GodTier_Developer_Roadmap|God-Tier Developer Roadmap]]**
- [[Magic_Navigation_Menu_Indicator|Magic Navigation Menu Indicator (HTML)]]

### Projects
- [Top C Projects in 2023](https://www.mygreatlearning.com/blog/top-c-projects/#online-voting-system)
- [Mini Project in C Library Management System](https://www.codewithc.com/mini-project-in-c-library-management-system/)
- [50+ C/C++ Projects with Source Code](https://www.codewithc.com/c-projects-with-source-code/)

### Random
- [Fandom Stories Website](https://archiveofourown.org/)
- [How to crate box mock-up in Photoshop](https://pin.it/5kLutM1)
- Freudan Slips of the Tongue
- [[Eisenhower_Matrix.png|Eisenhower Matrix]]

### YO
- [[PIXIVpunipuni|Punipuni's illustration/Manga]]
- [[PIXIVRodriGuez|RodriGuez NSFW]]
- [[FACEBOOKSamuel_Youn_Alice|Samuel Youn - Alice]]

<br>

---
**Git Commands**
Commands I use 9/10 times (all this is from memory so I may have made a mistake or two on the ordering of arguments if there are multiple):
1. `git add .` (Adds all files to the stage)
2. `git commit -m "blah blah blah"` (Adds files in the stage to a checkpoint that you can revert back to, with a message of blah blah blah to remind you what you did)
3. `git push` (Sends your commits to github or whatever service you are using)
4. `git pull` (Retrieves any new commits that you don't have locally from github or whatever service you are using)
5. `git pull fromBranch toBranch` (Pulls commits that are different from one branch into another branch so that merging two branches together is easy)
6. `git clone` (Just copy the command from the service you are using if you clone a repo, it's way easier)
7. `git rm filepath` (Removes a file from the stage when you add it by accident, example is if you add your file with passwords)
8. `git checkout -b branchName` (Creates a new branch for you to work on so your work on one feature doesn't interfere with another)
9. `git checkout branchName` (Changes to another branch you have created)
10. `git stash` (Puts all your changes in a temporary vault so you can retrieve them later, but I pretty much always use it to revert changes so I can checkout to another branch)
11. `git init` (Don't do this, it's way easier to create a repo in whatever service you are using and then clone it than deal with connecting a repo to the service you want to use)
12. `git status` (Checks what files are on the stage)
13. `git pop` (Takes the last stashed object and applies the changes)

Git is a way of creating a tree of code checkpoints so if you make mistakes you can revert back to a previous version that you know works and it makes working on a codebase with multiple people way easier. Github, Bitbucket, Gitlab are all services that use git to provide cloud storage so you can store your code somewhere else to make sharing easy and so that you will never lose your code completely. If you want to merge two branches of the tree together, it's best to use the service's GUI to do it. Always pull from the branch you want to merge your branch into to fix conflicts ahead of time. Try to keep branches small and focused on a single feature to make resolving merge conflicts easy. If you have to do anything other than what I listed in git, then you are in an awful place, and may whatever god you worship have mercy on your soul. Use stack overflow liberally in these situations.
source: [Is using Git difficult or am I just plain stupid? : learnprogramming (reddit.com)](https://www.reddit.com/r/learnprogramming/comments/x55c6q/is_using_git_difficult_or_am_i_just_plain_stupid/)

**BASH VS GIT**
`Bash` (**B**ourne-**A**gain-**SH**ell) - is a <mark class="hltr-lightgreen">Unix shell and command-line interpreter</mark> that provides an environment for executing commands and scripts.
`Git` - is a v<mark class="hltr-lightgreen">ersion control system</mark> that allows developers to keep track of changes to their code and collaborate with other developers on a project. It can be used from within a *bash shell* or from any other environment that supports *Git*.

**DEMANDED PROGRAMMING LANGUAGES**
As a backend developer, the most in-demand programming languages are typically Python, Java, and JavaScript (Node.js). Here's a brief overview of each language:
1.  Python: Python is a popular, high-level programming language that is widely used for server-side web development, scientific computing, data analysis, and artificial intelligence. It has a large, active community and a wealth of available libraries and frameworks that make it easy to get started.
2.  Java: Java is a mature, object-oriented programming language that is widely used for server-side web development, enterprise applications, and Android mobile app development. Java has a large, well-established ecosystem and is known for its stability, security, and performance.
3.  JavaScript (Node.js): JavaScript is a popular, dynamically-typed language that was originally designed for client-side web development. However, with the introduction of Node.js, it has become a popular choice for server-side development as well. JavaScript is known for its versatility and fast performance, and it's often used for real-time, scalable, and high-traffic applications.
PHP is also widely used for server-side web development, especially for building dynamic websites and content management systems (CMSs). However, it's less commonly used than the other three languages and may be less in demand in the job market.

In conclusion, the best language for you to invest in as a backend developer will depend on your personal preferences and the types of projects you want to work on. It's a good idea to familiarize yourself with multiple languages and frameworks to increase your chances of landing a job and staying marketable in the future.

**C++ Language Learning Techniques**
Here are some tips to help you get the most out of the C++ language:
1.  Understand the basics of object-oriented programming (OOP) and how it applies to C++. OOP is a programming paradigm that is heavily used in C++, and understanding the concepts of classes, objects, inheritance, and polymorphism is essential to writing good C++ code.
2.  Make use of the standard template library (STL) that comes with C++. The STL contains a wide range of useful data structures and algorithms that can save you a lot of time and effort when writing code.
3.  Learn how to use smart pointers. Smart pointers are a C++11 feature that can help you manage memory more effectively and prevent common issues such as memory leaks and segmentation faults.
4.  Understand the difference between pass by value and pass by reference. Knowing when to use each one can greatly improve the performance of your code.
5.  Use RAII (Resource Acquisition Is Initialization) technique where possible. The RAII technique ensures that resources are acquired and initialized at the time an object is constructed and are properly released when the object is destroyed.
6.  Understand the difference between **lvalue** and **rvalue** references. This can help you write more efficient code, particularly when working with move semantics and perfect forwarding.
7.  Familiarize yourself with the C++11 and C++14 features. C++11 and C++14 introduced many new features that can make your code more expressive and efficient.
8.  Be aware of the different types of initialization and how they work. The way you initialize your variables can have a big impact on the performance and correctness of your code.
9.  Always use the `const` keyword where possible. Using `const` can help prevent bugs and improve performance by making it clear when a value should not be modified.
10.  Write clear, readable, and well-organized code. This will make it easier to maintain and improve your code in the future.
    

Note that these are just a few tips to improve your C++ programming, and there are many more ways to improve your skills and write better code. It's always a good idea to continually learn and explore new features and libraries that the language offers.

## Dynamic Array of strings
```C
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main() {
    int size = 5;
    char **strArr = (char **)malloc(size * sizeof(char *));

    if (strArr == NULL) {
        printf("Memory allocation failed.\n");
        return 1;
    }

    // Allocate memory for each string
    for (int i = 0; i < size; i++) {
	    // Assume maximum string length of 50 characters
        strArr[i] = (char *)malloc(50 * sizeof(char));
    }

    // Initialize the strings
    strcpy(strArr[0], "Hello");
    strcpy(strArr[1], "World");
    strcpy(strArr[2], "OpenAI");
    strcpy(strArr[3], "ChatGPT");
    strcpy(strArr[4], "Example");

    // Print the strings
    for (int i = 0; i < size; i++) {
        printf("%s\n", strArr[i]);
    }

    // Free the dynamically allocated memory
    for (int i = 0; i < size; i++) {
        free(strArr[i]);
    }
    free(strArr);

    return 0;
}
```