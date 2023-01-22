---
title: C++class
creation-date: 2023-01-18
aliases:
tags:
- CPP/Lecture
- CPP/Class
- CPP/Library/cmath/pow
- CPP/const
---
**[[C++|HOME [C++]]]**

---
# Class
are user-defined types, defined by class-specifier, which appears in `decl-specifier-seq` of the declaration syntax.
> members initialized is set to `private` in default

**efficient way of using CLASS**
```cpp
class myClass {
private:
	int age;
public:
	myClass(int age_param) : age(age_param){}
};

int main() {
	myClass p1(20);

	std::cout << p1 << std::endl;

	return 0;
}
```

---
```cpp
#include <iostream>
#include <cmath>
const double PI{3.1415926535897932384626433832795};

class cylinder {
private:
	// Inaccessible outside of scope
    double base_radius{1.0}, height{1.0}; // Member variables

public:
    double volume() { return PI * pow(base_radius, 2) * height; }
};

int main(int argc, char **argv) {
    cylinder func1; // creating Objects

    std::cout << "volume1: " << func1.volume() << std::endl;
    return 0;
}
```

>[!FAQ|alt-co]+
>- Class member variables can either be raw stack variables or pointers
>- <mark class="hltr-blue">Members can't be references</mark>
>- Classes have functions (methods) that let them do things
>- Class methods <u>have access to the member</u> variables, <u>regardless</u> of whether <u>they are public/private</u>
>- Private members of classes (variables and functions) aren't accessible from the outside of the class definition

<br>

# 
---
**Sources:**
- **classes** - https://en.cppreference.com/w/cpp/language/classes
- **class declaration** - https://en.cppreference.com/w/cpp/language/class
- **access specifier** - https://en.cppreference.com/w/cpp/language/access