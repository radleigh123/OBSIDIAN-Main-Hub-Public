---
title: C++string
creation-date: 2023-01-12
aliases:
tags:
- CPP/Lecture
- CPP/Library/string/string
- CPP/References
- CPP/Library/string_view/string_view
---
**[[C++|HOME [C++]]]**

---
# `std::string`
```cpp
#include <iostream>
#include <string>

int main() {
    // Empty string
    std::string full_name;
    // Initialized with string literal
    std::string planet{"Earth. The sky is blue"};

    std::string preferred_plant{planet};
    // Initialized with part of a string literal. Contains "Hello"
    std::string message{"Hello there", 5};
    // Initialized with multiple copies of a char. Contains "eeee"
    std::string weird_message{4, 'e'};

    std::string greeting{"Hello Earth"};
    // Initialized with part of an existing string at index 6, taking 5 characters. Contains "Earth"
    std::string saying_hello{greeting, 6, 5};

    std::cout << "full_name: " << full_name << std::endl;
    std::cout << "planet: " << planet << std::endl;
    std::cout << "preferred_planet: " << preferred_plant << std::endl;
    std::cout << "message: " << message << std::endl;
    std::cout << "weird_message: " << weird_message << std::endl;
    std::cout << "greeting: " << greeting << std::endl;
    std::cout << "saying_hello: " << saying_hello << std::endl;

    return 0;
}
```

>[!CHECK|alt-co] Changing `std::string` at runtime is valid
> ```cpp
> planet = "The fox jumped over the fence. Humpty Dumpty sat on the wall, humpy dumpty had a great fall";
> // despite the size being greater than what was initialized
> ```

## Differences between `std::string_view` and [[C++references|references]]
```cpp
#include <iostream>
#include <string>
#include <string_view>

void printString(std::string_view sv) { std::cout << sv << std::endl; }
void printStringRef(const std::string &str) { std::cout << str << std::endl; }

int main() {
    std::string myString = "Hello, world!";

    // Using std::string_view
    std::string_view sv = myString; // creates a string_view to myString
    printString(sv);                // prints "Hello, world!"
    printString(sv.substr(7));      // prints "world!"
    sv = "Goodbye";                 // the value of myString is not affected
    printString(sv);                // prints "Goodbye"
    printString(myString);          // prints "Hello, world!"
    // While in case of string_view, it does not affect the original string and it can be assigned with a new value

    // Using a reference
    const std::string &str = myString; // create a reference to myString
    printStringRef(str);               // prints "Hello, world!"
    printStringRef(str.substr(7));     // prints "world!"
    str = "Goodbye";                   // This will cause a compile error, as it is const reference.

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/string/basic_string
- **string_view** - https://en.cppreference.com/w/cpp/string/basic_string_view