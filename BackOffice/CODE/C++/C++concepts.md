---
title: C++concepts
creation-date: 2023-01-17
aliases:
tags:
- CPP/Lecture
- CPP/Library/concepts
---
**[[C++|HOME [C++]]]**

---
# Concepts
a mechanism to place constraints on your template type parameters (C++ 20)
>[!column|collapse ttl-c clean no-t]
>>[!INFO|clean no-i] <mark class="hltr-blue">Standard built-in concepts</mark>
>
>>[!INFO|clean no-i] Custom concepts

<br>

**e.g. an alternative to static asserts and type traits**
```cpp
template <typename T>
void print_number(T n) {
	static_assert(std::is_integral<T>::value, "Must pass in an integral argument");
	std::cout << "n: " << n << std::endl;
}
```
- [[C++conceptsintegral|integral]] - specifies that a type is an integral type

<br>

# 
---
**Sources:**
- **Concepts library** - https://en.cppreference.com/w/cpp/concepts