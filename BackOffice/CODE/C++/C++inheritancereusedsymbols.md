---
aliases:
tags:
- CPP/Lecture
- CPP/Class/Inheritance
---
**[[C++|HOME [C++]]]**

---
## Reused symbols in Inheritance
is a compiler error that occurs when a derived class uses the same name for a variable, function or other member as a member in its base class.

```cpp
class Base {
public:
    Base(int a) : m_num1(a) {}
    void print_info() { std::cout << "Base: " << m_num1 << std::endl; }

private:
    int m_num1{}; // 150
};

class Derived : public Base {
public:
    Derived(int a) : Base(a) {}
	// Derived(int a) : m_num1(a) {} // ERROR!
	// m_num1 is hiding the inherited m_num1 from the Base class

    void print_info() { std::cout << "Derived: " << m_num1 << std::endl; }

private:
    int m_num1{}; // junk value
};

f1.Base::print_info(); // cals the method in Child
f1.print_info(); // calls the method in Parent
```