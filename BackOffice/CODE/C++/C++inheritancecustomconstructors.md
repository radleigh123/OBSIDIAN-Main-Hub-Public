---
aliases:
tags:
- CPP/Lecture
- CPP/Class/Constructor
- CPP/Class/Inheritance
---
**[[C++|HOME [C++]]]**

---
## Custom constructors with inheritance
![[Pasted image 20230125181455.png|center wm-tl cover]]

>[!FAIL|alt-co ttl-c] base data members not belonging to derived class
> ```cpp
> derivedClass::derivedClass(int a, int b) : m_num1(a), m_num2(b) {}
> ```

>[!CHECK]+ calling base constructor
> ```cpp
> class baseClass {
> private:
>     int m_num1{};
>     double m_num2{};
> 
> public:
>     baseClass(int a, double b) : m_num1(a), m_num2(b) {}
> };
> 
> class Derived : public baseClass {
> public:
>     Derived(int dera, double derb) : baseClass(dera, derb) {}
>     // despite the PRIVATE access level, using initializer list helps
>     // m_num1 = dera
>     // m_num2 = derb
> };
> ```