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

int main() {
    MyClass obj;

    // Declare a pointer to a member function of MyClass
    void (MyClass::*ptr)() = &MyClass::func2;

    // Call the member function through the pointer
    (obj.*ptr)();  // Output: "Inside func2"

    return 0;
}
```