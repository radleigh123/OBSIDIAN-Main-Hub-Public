---
aliases:
tags:
- CPP/Lecture
- CPP/Class/Constructor
- CPP/Class/Inheritance
---
**[[C++|HOME [C++]]]**

---
## Inheriting base constructors
when a derived class inherits the base constructor, it means that the derived class will use the constructor of the base class automatically, without the need to explicitly call it.
**e.g.**
```cpp
class Base {
private:
	int m_num{};

public:
    Base(int x) : m_num(x) {}
	int get_m_num() { return m_num; }
};

class Derived : public Base {
public:
    using Base::Base;
};

Derived d(5);  // calls Base::Base(5)
std::cout << d.get_m_num() << std::endl;
```
<br>

>[!WARNING|alt-co]+
> Inheriting constructors adds a level of confusion to your code, its not clear which constructor is building your object. It is recommended to avoid using them and only use this feature if necessary