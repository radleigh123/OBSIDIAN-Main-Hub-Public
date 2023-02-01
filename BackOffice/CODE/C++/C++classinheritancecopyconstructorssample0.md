---
aliases:
tags:
- CPP/Class/Constructor/Copy
- CPP/Class/Destructor
- CPP/Library/stringh
- CPP/Pointers
---
**[[C++inheritancecopyconstructors|BACK]]**

---
>[!recite|clean no-i] Copy constructor with pointers & strings

```cpp
#include <iostream>
#include <string.h>

class myString {
private:
    char *m_value;

public:
    myString(const char *value_param) {
        m_value = new char[strlen(value_param) + 1]; // allocate memory for new string
        strcpy(m_value, value_param);
    }

    myString(const myString &other) {
        m_value = new char[strlen(other.m_value) + 1]; // allocate memory for new string
        strcpy(m_value, other.m_value);
    }

    ~myString() {
        delete[] m_value; // deallocate memory when object is destroyed
    }

    const char *get_m_value() const { return m_value; }
};

int main() {
    myString f1("Hello World");
    myString f2 = f1; // copy constructor called...

    std::cout << f2.get_m_value() << std::endl;

    return 0;
}
```