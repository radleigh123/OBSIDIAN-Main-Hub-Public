---
aliases:
tags:
- CPP/Lecture
- CPP/Functions/lambda
---
**[[C++functionslambda|BACK]]**

---
## Lambda function sample 2
```cpp
#include <iostream>

int main(int argc, char **argv) {
    auto result = [](double num1, double num2){
        return (num1 + num2);
    }(12.5489, 5.1211);

    std::cout << "result: " << result;

	/*
	// Alternative for multiple calls
	auto result = [](double num1, double num2){
        return (num1 + num2);
    };

    std::cout << "result: " << result(12.5489, 5.1211);
	*/

    /*
    // Print immediately
    std::cout << "result: " << [](double num1, double num2){
        return (num1 + num2);
    }(12.5489, 5.1211);
    */
    return 0;
}
```