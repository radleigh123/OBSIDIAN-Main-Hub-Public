```cpp
#include <iostream>

class MyClass {
public:
    int data;
    MyClass() { std::cout << "MyClass constructor called" << std::endl; }
    ~MyClass() { std::cout << "MyClass destructor called" << std::endl; }
};

int main() {
    MyClass obj;
    obj.data = 5;

    // Declare a pointer to a member object of MyClass
    int MyClass::*ptr = &MyClass::data;

    // Access the member object through the pointer
    std::cout << obj.*ptr << std::endl;  // Output: 5

    return 0;
}
```
In this example, `MyClass` has an `int` data member named `data`, and a constructor and a destructor, which are called when an object of the class is created and destroyed respectively. In the `main()` function, an object of the class `MyClass` is created, and its `data` member is assigned the value 5. Then, a pointer `ptr` is declared, which points to the address of `MyClass::data`. The member object is then accessed through the pointer `obj.*ptr`.
<br>

You can also access the member object through a pointer object like this:
```cpp
MyClass *pObj = &obj;
std::cout << pObj->*ptr << std::endl;  // Output: 5
```
The `->*` operator is used to access the member object through the pointer object `pObj` and the `ptr` pointer to member.