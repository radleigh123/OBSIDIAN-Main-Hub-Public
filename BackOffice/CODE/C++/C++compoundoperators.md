---
aliases:
tags:
- CPP/Lecture
- CPP/Operators
---
**[[C++|HOME[C++]]]**

---
## Compound operators
or Assignment operators

>[!column|clean no-t collapse]
>>[!INFO|clean no-t txt-c]
>> **Addition**
>> `+=`
>> **Subtraction**
>> `-=`
>> **Multiplication**
>> `*=`
>
>>[!INFO|clean no-t txt-c]
>> **Division**
>> `/=`
>> **Modulo**
>> `%=`

```cpp
#include <iostream>

int main()
{
    int num1{5}, num2{10};
    num1 *= num2 += num1;

    std::cout << num1 << std::endl;
    return 0;
}
```

<br>

# 
---
**Sources:**
- Learn more about **[[C++precedence&associativity|precedency and associativity]]**