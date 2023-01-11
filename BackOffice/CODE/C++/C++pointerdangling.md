---
aliases:
tags:
- CPP/Lecture
- CPP/Pointers
- CPP/Expressions/delete
---
**[[C++|HOME [C++]]]**

---
## Dangling pointers
a pointer that doesn't point to valid memory address
>[!FAIL|alt-co]- Deleted pointer
> ```cpp
> #include <iostream>
> int main()
> {
> 	std::cout << "Deleted pointer\n";
> 	int *ptr_var1{new int{65}};
> 	
> 	std::cout << "*ptr_var1 (before delete): " << *ptr_var1 << std::endl;
> 	
> 	delete ptr_var1;
> 	std::cout << "*ptr_var1 (after delete): " << *ptr_var1 << std::endl;
> 	
> 	return 0;
> }
> ```

>[!FAIL|alt-co]- Multiple pointers pointing to same address
> ```cpp
> #include <iostream>
> 
> int main()
> {
> 	std::cout << "Multiple pointers pointing to same address\n";
> 	int *ptr_var1{new int{84}};
> 	int *ptr_var2{ptr_var1};
>
> 	std::cout << "ptr_var1: " << ptr_var1 << "\t" << *ptr_var1 << std::endl;
> 	std::cout << "ptr_var2: " << ptr_var2 << "\t" << *ptr_var2 << std::endl;
>
> 	delete ptr_var1;
>
> 	// ptr_var2 points to delete memory
> 	std::cout << "\nptr_var2 (after deleting ptr_var1): " << ptr_var2 << "\t" << *ptr_var2 << std::endl;
>
> 	return 0;
> }
> ```

**Solution 1** - initialize your pointers upon declaration
```cpp
#include <iostream>

int main()
{
    int *ptr_var1{};
    int *ptr_var2{new int{45}};

    // Check for nullptr before use
    if (ptr_var1 != nullptr)
        std::cout << "*ptr_var1: " << *ptr_var1 << std::endl;

    return 0;
}
```

---
**Solution 2** - Make sure there is one clear pointer (master ptr) that owns the memory (responsible for releasing when necessary), other pointers should only be able to dereference when the master ptr is valid
```cpp
#include <iostream>

int main()
{
    int *ptr_var1{new int{45}};
    int *ptr_var2{ptr_var1};

    // Dereference the pointers and use time
    std::cout << "ptr_var1 - " << ptr_var1 << " - " << *ptr_var1 << std::endl;

    // Only use slave pointers when master ptr is valid
    if (!(ptr_var1 == nullptr))
        std::cout << "ptr_var2 - " << ptr_var2 << " - " << *ptr_var2 << std::endl;

    delete ptr_var1; // master releases the memory
    ptr_var1 = nullptr;

    // Only use slave pointers when master ptr is valid
    if (!(ptr_var1 == nullptr))
        std::cout << "ptr_var2 - " << ptr_var2 << " - " << *ptr_var2 << std::endl;
    else
        std::cerr << "WARNING: Trying to use an invalid pointer";

    return 0;
}
```