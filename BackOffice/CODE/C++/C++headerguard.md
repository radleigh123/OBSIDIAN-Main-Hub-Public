---
aliases:
tags:
- CPP/Lecture
- CPP/Preprocessor
---
**[[C++|HOME [C++]]]**

---
## Header guard
The use of a class with member functions and multiple files:

**MyClass.h**
```cpp
#ifndef MYCLASS_H
#define MYCLASS_H

class MyClass {
public:
    int x;
    void setX(int value);
    int getX();
};

#endif
```
**MyClass.cpp**
```cpp
#include "MyClass.h"

void MyClass::setX(int value) {
    x = value;
}

int MyClass::getX() {
    return x;
}
```
**main.cpp**
```cpp
#include <iostream>
#include "MyClass.h"

int main() {
    MyClass obj;
    obj.setX(5);
    std::cout << obj.getX() << std::endl;
    return 0;
}
```

>[!FAQ|ttl-c alt-co bg-blue] Preprocessor macros: why in uppercase letters
> The use of all uppercase letters for preprocessor macros is a convention that is commonly used in C++ to distinguish them from variables and functions. By convention, preprocessor macro names are typically written in uppercase letters, while variable and function names are written in lowercase letters.
> 
> The reason behind this is that preprocessor macros are a separate concept from variables and functions, and they are processed by the preprocessor before the program is compiled. By using all uppercase letters, it makes it easier to spot preprocessor macros in the code, and it can help to prevent naming conflicts between preprocessor macros and variables or functions.
> 
> The preprocessor "MYCLASS_H" is an example of a **header guard**, it is a preprocessor directive that prevents a header file from being included more than once in a single compilation unit. <mark class="hltr-blue">It is a common technique used to prevent multiple definitions of functions or variables that are defined in the header file</mark>.
> 
> In this example, the "MYCLASS_H" is used as an identifier for the header file, to make sure that the header file is included only once. The preprocessor directive "#ifndef MYCLASS_H" checks if the MYCLASS_H macro is not defined, and if it is not, the preprocessor defines it and continues to include the contents of the header file. If MYCLASS_H is already defined, the preprocessor skips the contents of the header file.