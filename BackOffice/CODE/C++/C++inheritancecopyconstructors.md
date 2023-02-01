---
aliases:
tags:
- CPP/Lecture
- CPP/Class/Constructor/InitializerList
- CPP/Class/Inheritance
---
**[[C++|HOME [C++]]]**

---
## Copy constructors with inheritance
initializes an object by copying the member values from an object of the same type.
**e.g.**
```cpp
class baseClass {
public:
    baseClass(int a, int b) : m_num1(a), m_num2(b) {}
    baseClass(const baseClass &other) : m_num1(other.m_num1), m_num2(other.m_num2) {}

    int get_m_num1() { return m_num1; }
    int get_m_num2() { return m_num2; }

private:
    int m_num1{};
    int m_num2{};
};

class derivedClass : public baseClass {
public:
    derivedClass(int c, int d, double e) : baseClass(c, d), der_num3(e) {}
    derivedClass(const derivedClass &der_other) : baseClass(der_other), der_num3(der_other.der_num3) {}

    double get_der_num3() { return der_num3; }

private:
    double der_num3{};
};

int main() {
    derivedClass f1(150, 400, 5.35);
    derivedClass f2 = f1; // copy constructor called

    std::cout << f2.get_m_num1() << " " << f2.get_m_num2() << " " << f2.get_der_num3() << std::endl;

    return 0;
}
```
<br>

- [[C++classinheritancecopyconstructorssample0|Copy constructor with pointers & strings]]

<br>

# 
---
**Sources:**
- https://learn.microsoft.com/en-us/cpp/cpp/constructors-cpp?view=msvc-170#copy_and_move_constructors