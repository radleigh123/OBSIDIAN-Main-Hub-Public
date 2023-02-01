---
aliases:
tags:
- CPP/Pointers
- CPP/typedef
---
**[[C++classpointers|BACK]]**

---
## Declaring pointer using [[C++typedef|typedef]]

>[!aside|right]+
> MyClass constructor called
> Inside func2
> MyClass destructor called
```cpp
#include <iostream>

class MyClass {
public:
    MyClass() { std::cout << "MyClass constructor called" << std::endl; }
    ~MyClass() { std::cout << "MyClass destructor called" << std::endl; }

    void func1() { std::cout << "Inside func1" << std::endl; }
    void func2() { std::cout << "Inside func2" << std::endl; }
    void func3() { std::cout << "Inside func3" << std::endl; }
};

typedef void (MyClass::*MyClassFunc) ();

int main() {
    MyClass obj;

    // Declare a pointer to a member function of MyClass
    MyClassFunc ptr = &MyClass::func2;

    // Call the member function through the pointer
    (obj.*ptr)();  // Output: "Inside func2"

    return 0;
}
```

In this example, I've defined a typedef named `MyClassFunc` which is a pointer to a member function of `MyClass` that returns void and takes no arguments. Later, I declare `ptr` of type `MyClassFunc` and initialize it with the address of the `func2` member function. The rest of the program works the same way as before.
<br>

You can also use `using` keyword C++11 and later to define a typedef like this:
```cpp
using MyClassFunc = void (MyClass::*)();
```
The advantage of this approach is that it makes the code more readable and maintainable. You can easily identify that `ptr` is a pointer to a member function of `MyClass` by looking at the type.