---
aliases:
tags:
- CPP/Lecture
- CPP/Pointers
---
**[[C++|HOME [C++]]]**

---
## Pointer to char
```cpp
#include <iostream>

int main()
{
    char *char_ptr{nullptr};
    char char_var1{'A'};
    char_ptr = &char_var1;

    std::cout << "&char_var1: " << reinterpret_cast<void *>(&char_var1) << std::endl;
    std::cout << "char_ptr: " << reinterpret_cast<void *>(char_ptr) << std::endl;
    std::cout << "char_var1: " << *char_ptr << std::endl;

    char char_var2{'a'};
    char_ptr = &char_var2;

    std::cout << "\n&char_var2: " << reinterpret_cast<void *>(&char_var2) << std::endl;
    std::cout << "char_ptr: " << reinterpret_cast<void *>(char_ptr) << std::endl;
    std::cout << "char_var2: " << *char_ptr << std::endl;

    return 0;
}
```
>[!INFO]+ Can also initialize with a string literal
> ```cpp
> #include <iostream>
> 
> int main()
> {
> 	char *ptr_str{"Hello World"};
> 	
> 	std::cout << ptr_str;
> 	std::cout << *ptr_str; // Only prints 'H'
> 	
> 	return 0;
> }
> ```

**Regular array notation** & **Pointer Arithmetic** both works either way:
>[!column|no-t clean collapse]
>>[!INFO|clean no-t]
>> `&ptr_str[0] = ptr_str;`
>> `&ptr_str[i] = ptr_str + i;`
>
>>[!INFO|clean no-t]
>> `ptr_str[0] = *ptr_str;`
>> `ptr_str[i] = *(ptr_str + i);`