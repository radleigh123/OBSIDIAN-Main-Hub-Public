---
title: C++switch
creation-date: 2023-01-08
aliases:
tags:
- CPP/Lecture
- CPP/FlowControl/switch
---
**[[C++|HOME [C++]]]**

---
# Switch statement
Transfers control to one of several statements, depending on the value of a condition.

```cpp
#include <iostream>

// Tools
const int Pen{1};
const int Marker{2};
const int Eraser{3};
const int Rectangle{4};
const int Circle{5};
const int Ellipse{6};

int main()
{
    int user_input;
    std::cout << "Enter tool: ";
    std::cin >> user_input;

    switch (user_input)
    {
    case Pen:
        std::cout << "Active tool is Pen" << std::endl;
        break;
    case Marker:
        std::cout << "Active tool is Marker" << std::endl;
        break;
    case Eraser:
        std::cout << "Active tool is Eraser" << std::endl;
        break;
    case Rectangle:
        std::cout << "Active tool is Rectangle" << std::endl;
        break;
    case Circle:
        std::cout << "Active tool is Circle" << std::endl;
        break;
    case Ellipse:
        std::cout << "Active tool is Ellipse" << std::endl;
        break;
    default:
        std::cout << "For eval" << std::endl;
        break;
    }

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/language/switch