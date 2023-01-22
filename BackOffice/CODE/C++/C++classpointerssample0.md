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

int main() {
    MyClass obj;
    MyClass *pObj = &obj;

    // Call the member function through the pointer object
    (pObj->*&MyClass::func2)();  // Output: "Inside func2"

    return 0;
}
```