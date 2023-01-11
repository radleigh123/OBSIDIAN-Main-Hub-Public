---
aliases:
tags:
- CPP/Lecture
- CPP/Pointers
- CPP/Arrays
- CPP/Expressions/new
- CPP/Expressions/delete
---
**[[C++|HOME [C++]]]**

---
## Dynamic arrays
A dynamic array variable holds a pointer to an array value.
- are allocated at run time
- size is not fixed
- located in Heap memory space

**e.g.** `int *foo{new int[10]};`

>[!EXAMPLE]- Array dynamic allocation
> ```cpp
> #include <iostream>
> 
> int main() {
>     const size_t size{10};
> 
>     // Declaring arrays in different ways
> 
>     // will contain garbage values
>     double *ptr_salaries{new double[size]};
> 
>     // all values initialized to 0
>     int *ptr_students{new (std::nothrow) int[size]{}};
> 
>     // Allocating memory space for an array of size double variables
>     double *ptr_scores{new (std::nothrow) double[size]{1, 2, 3, 4, 5, 6, 7, 8, 9, 10}};
> 
>     // check `nullptr` and use the allocated array
>     if (ptr_scores) {
>         for (size_t i = 0; i < size; i++) {
>             std::cout << "value: " << *(ptr_scores + i) << std::endl;
>         }
>     }
> 
>     // Releasing memory for arrays
>     delete[] ptr_salaries;
>     ptr_salaries = nullptr;
>     delete[] ptr_students;
>     ptr_students = nullptr;
>     delete[] ptr_scores;
>     ptr_scores = nullptr;
> 
>     return 0;
> }
> ```

## Static Arrays
A static array variable holds a value of type, array.
- are allocated memory at compile time
- located in Stack memory space

**e.g.** `int foo[10];` // array of size 10


<br>

# 
---
**Sources:**
- [Comparison of Static and Dynamic Arrays](https://www.vtscada.com/help/Content/Scripting/ValueTypes/StaticVsDynamicArrays.htm#:~:text=A%20static%20array%20variable%20holds,use%20either%20type%20of%20array.)
- https://stackoverflow.com/questions/2672085/what-is-the-difference-between-static-and-dynamic-arrays-in-c