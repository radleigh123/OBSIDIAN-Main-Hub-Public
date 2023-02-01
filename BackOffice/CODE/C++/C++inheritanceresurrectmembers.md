---
aliases:
tags:
- CPP/Lecture
- CPP/Class/Inheritance
- CPP/Class/BaseClassAccessSpecifier/private
---
**[[C++|HOME [C++]]]**

---
## Resurrecting members back in scope
>[!WARNING|alt-co] PROCEED WITH CAUTION
>- This approach is considered a bad practice because it breaks encapsulation of the class.

**Accessing using the `using` keyword**
```cpp
class baseClass {
private:
    int private_member{59}; // private member

public:
    int get_private_member() { return private_member; }
};

class derivedClass : public baseClass {
public:
    int get_derived_private_member() { return get_private_member(); } // "resurrects" private_member
};
```

**Accessing using `friend`**
```cpp

```
<br>

---
- [A] [[C++classinheritanceresurrectmemberssample0|RECOMMENDED ALTERNATIVES]]