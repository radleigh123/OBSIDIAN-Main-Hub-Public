---
cssclass: t-c, tbl-nalt
title: C++inputoutput
creation-date: 2023-01-06
aliases:
tags:
- CPP/Lecture
- CPP/Library/string/getline
- CPP/Library/io
---
**[[C++|HOME [C++]]]**

---
# Input & Output

| stream      | meaning                              |
| ----------- | ------------------------------------ |
| `std::cout` | prints data to the console           |
| `std::cin`  | reads data from the console          |
| `std::cerr` | prints *errors* to the console       |
| `std::clog` | prints *log messages* to the console |

## Printing data
```cpp
#include <iostream>

int main()
{
    int age{21};
    std::cout << "The age is: " << age << std::endl;

    std::cerr << "Something went wrong" << std::endl; // Error

    std::clog << "This is a log message" << std::endl; // Log message

    return 0;
}
```

## Reading data
```cpp
#include <iostream>
#include <string>

int main()
{
    int age;
    std::string name;

    std::cout << "Your full name: " << std::endl;
    std::getline(std::cin, name);

    std::cout << "Your age: " << std::endl;
    std::cin >> age;

    /*
    std::cout << "Your name and age: " << std::endl;
    std::cin >> name >> age; // input both variables
    */

    std::cout << "Hello " << name << "\n"
              << age << " years old" << std::endl;

    return 0;
}
```