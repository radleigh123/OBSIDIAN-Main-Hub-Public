---
aliases:
tags:
- CPP/Lecture
- CPP/Class
- CPP/Pointers
---
**[[C++|HOME [C++]]]**

---
## The this pointer
Each class member function contains a hidden pointer called this. That pointer contains the address of the current object, for which the method is being executed. This also applies to constructors and destructors
**e.g.**
```cpp
#include <iostream>

class MyClass {
public:
    int x;
    void setX(int x) {
        // Assign the value of the local variable x to the member variable x
        this->x = x;
    }
    void printX() {
        // Local variable x shadows the member variable x
        int x = 20; 
        // Use the this pointer to access the member variable x
        std::cout << "The value of x is " << this->x << std::endl;
    }
};

int main() {
    MyClass obj;
    obj.setX(5);
    obj.printX(); // result: The value of x is 5
    return 0;
}
```

**Example**
- [[C++classthethispointersample1|Printing out object addresses]]
- [[C++classthethispointersample2|Using getters & setters]]
- [[C++classthethispointersample3|Chained calls using pointers]]

<br>

# 
---
 **Source:**
 - https://en.cppreference.com/w/cpp/language/this