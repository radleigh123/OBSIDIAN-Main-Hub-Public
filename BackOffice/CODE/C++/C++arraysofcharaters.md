---
aliases:
tags:
- CPP/Lecture
- CPP/Arrays
- CPP/Strings
- CPP/size
---
**[[C++|HOME [C++]]]**

---
## Array of characters
```cpp
#include <iostream>

int main()
{
    char arr1[]{'E', 'a', 'r', 'z', 'h'};
    arr1[3] = 't';
    std::cout << "size(arr1):\t" << std::size(arr1) << std::endl;
    std::cout << "sizeof(arr1):\t" << sizeof(arr1) << std::endl;

    std::cout << std::endl;
    for (auto &i : arr1)
    {
        std::cout << i;
    }

    return 0;
}
```

>[!INFO|alt-co]+ Declaring and Initializing a string
> ```cpp
> #include <iostream>
> 
> int main() {
> 	// or char arr1[6]{'E', 'a', 'r', 'z', 'h'}
> 	char arr1[]{'E', 'a', 'r', 'z', 'h', '\0'};
> 	
> 	std::cout << "sizeof(arr1): " << sizeof(arr1) << std::endl;
> 	std::cout << arr1;
> 	
> 	return 0;
> }
> ```

>[!INFO|alt-co]+ Can also define a literal C string
> ```cpp
> #include <iostream>
> 
> int main() {
> 	// an implicit '\0' character is appended to the end of the string, making it a C string
> 	char str1[]{"Hello World"};
> 	
> 	std::cout << "str1: " << str1 << std::endl;
> 	std::cout << "size(str1): " << std::size(str1);
> 	
> 	return 0;
> }
> ```