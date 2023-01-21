---
title: C++functions
creation-date: 2023-01-12
aliases:
tags:
- CPP/Lecture
- CPP/Functions
---
**[[C++|HOME [C++]]]**

---
# Functions
are C++ entities that associate a sequence of statements (a function body) with a name and a list of zero or more function parameters
```cpp
#include <iostream>
bool isodd(int); // function declaration

int main() {
	isodd(50); // function call

	return 0;
}

// function definition/implementation
// parameter list has one parameter, with name "n" and type int
// the return type is bool
bool isodd(int n) {
    return n % 2;
}
```



<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/language/functions