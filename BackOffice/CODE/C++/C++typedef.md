---
title: C++typedef
creation-date: 2023-01-29
aliases:
tags:
- CPP/Lecture
- CPP/typedef
---
**[[C++|HOME [C++]]]**

---
# `typedef` specifier
is a keyword that allows you to create an alias for an existing data type.
**Syntax:**
```cpp
typedef existing_type new_type_name;
```

**e.g.**
```cpp
typedef int MyInt;
MyInt x = 5;
```
>[!column|flex clean no-t]
>>[!INFO|clean no-i ttl-c] create type alias template
>> ```cpp
>> template<typename T>
>> using MyVector = std::vector<T>;
>> ```
>
>>[!INFO|clean no-i ttl-c] used with pointers or classes
>> ```cpp
>> #include <iostream>
>> 
>> class myClass {
>> public:
>> 	int x;
>> };
>> 
>> typedef myClass *myClass_ptr;
>> 
>> int main(int argc, char **argv) {
>> 	myClass_ptr ptr = new myClass();
>> 	ptr->x = 10;
>> 	
>> 	std::cout << ptr->x;
>> 	return 0;
>> }
>> ```
<br>

# 
---
**Sources**
- https://en.cppreference.com/w/cpp/language/typedef