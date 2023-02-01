---
aliases:
tags:
- CPP/Lecture
- CPP/Library/initializer_list/initializer_list
---
**[[C++|HOME [C++]]]**

---
## `std::initializer_list`
is a template class in C++ that represents an object of a list of values. It is a lightweight proxy object that provides access to an array of objects of type `const T`.
**initialize an object of a class with an <u>aggregate-initialization-enabled constructor</u>:**
```cpp
class MyClass {
public:
    MyClass(std::initializer_list<int> list) {
        for (const auto &value : list) {
            std::cout << value << " ";
        }
    }
};

void printList(std::initializer_list<int> list) {
	for (const auto &value : list) {
		std::cout << value << " ";
	}
}

int main() {
    // Initialize an object of MyClass with a list of values
    MyClass obj {1, 2, 3, 4, 5}; // Output: 1 2 3 4 5

	printList({1, 2, 3, 4, 5}); // Output: 1 2 3 4 5

    return 0;
}
```

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/utility/initializer_list