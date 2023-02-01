---
title: C++classdestructors
creation-date: 2023-01-19
aliases:
tags:
- CPP/Lecture
- CPP/Class/Destructor
- CPP/Pointers
- CPP/Library/string_view/string_view
---
**[[C++|HOME [C++]]]**

---
# Class: Destructors
>[!INFO|alt-co]+ When are destructors called
> are called in weird places that may not be obvious
>- When an object is passed by value to a function
>- When a local object is returned from a function (for some compilers)
>
> other obvious cases are:
>- When a local stack object goes out of scope (dies)
>- When a heap object is released with delete

**e.g.**
>[!aside|right]+
> Constructor called!
> Desstructor called!

```cpp
#include <iostream>

class MyClass {
public:
    MyClass() { std::cout << "Constructor called!" << std::endl; }
    
    ~MyClass() { std::cout << "Destructor called!" << std::endl; }
};

int main() {
    MyClass obj;
    return 0;
}
```
<br>

```cpp
#include <iostream>
#include <string_view>

class person {
public:
    person() = default;
    person(std::string_view name_param, std::string_view age_param, int grade_param);
    ~person();

private:
    std::string name, age;
    int *ptr_grade{nullptr};
};

person::person(std::string_view name_param, std::string_view age_param, int grade_param) {
    name = name_param;
    age = age_param;
    ptr_grade = new int; // `new` allocate memory from the heap
    *ptr_grade = grade_param;
    std::cout << "person constructor called for " << name << std::endl;
}

person::~person() {
    delete ptr_grade;
    std::cout << "person destructor called for " << name << std::endl;
}

void func1() {
    person *ptr_p = new person("Keane", "Radleigh", 45);
    delete ptr_p; // for the destructor of person to be called
}

int main() {
    func1();

    std::cout << "Done" << std::endl;
    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/language/destructor