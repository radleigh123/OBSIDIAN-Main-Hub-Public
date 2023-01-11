---
title: C++statements&functions
creation-date: 2023-01-06
aliases:
tags:
- CPP/Lecture
---
**[[C++|HOME [C++]]]**

---
# Statements & Functions
![[C++basicparts.excalidraw.svg|center]]

```cpp
#include <iostream>
int addNumbers(int, int);

int main()
{
    int num1 = 10, num2 = 5;
    std::cout << "First number: " << num1 << std::endl;
    std::cout << "Second number: " << num2 << std::endl;

    std::cout << "\nSum: " << addNumbers(num1, num2) << std::end;
    return 0;
}

int addNumbers(int a, int b)
{
    return a + b;
}
```

<br>

# 
---
**Sources:**
- **statements** -  https://en.cppreference.com/w/cpp/language/statements