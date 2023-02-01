---
aliases:
tags:
- CPP/Class/Inheritance
- CPP/Class/Constructor/get
- CPP/Class/Constructor/set
---
**[[C++inheritancebaseclassaccessspecifier|BACK]]**

---
>[!recite|clean no-i] Basic sample

```cpp
#include <iostream>

class myClass {
public:
    // Public member, accessible by both the base and derived class
    int var_public{10};

    // getter
    int get_var_private() { return var_private; }
    // setter
    void set_var_private(int var_param) { var_private = var_param; }

private:
    // Private member, not accessible by the derived class
    int var_private{20};

protected:
    // Protected member, accessible by the base and derived class
    int var_protected{30};
};

class derived_myClass : public myClass {
public:
    // Accessing protected member area from the derived class
    void print() { std::cout << var_protected << std::endl; }

    // Can't access PRIVATE member from the base class
    // void print2() { var_private = 100; }
};

int main() {
    derived_myClass f1;
    /*
    f1.var_private = 5; // PRIVATE! inaccessible
    f1.var_protected = 5; // PROTECTED! inaccessible
    */

    f1.print(); // 30

    f1.set_var_private(60);
    std::cout << f1.get_var_private() << std::endl; // 60

    return 0;
}
```