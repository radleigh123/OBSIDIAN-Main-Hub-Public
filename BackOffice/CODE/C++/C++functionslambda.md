---
title: C++functionslambda
creation-date: 2023-01-13
aliases:
tags:
- CPP/Lecture
- CPP/Functions/lambda
---
**[[C++|HOME [C++]]]**

---
# Lambda functions
a mechanism to set up anonymous [[C++functions|functions]](w/out names). Once we have them set up, we can either give them names and call them, or we can even get them to do things directly.
**Syntax:**
```cpp
[ captures ] ( params ) specs requires(optional) { body } // 1

[ captures ] { body } // 2
[ captures ] specs { body } // 2

[ captures ] < tparams > requires(optional) ( params ) specs requires(optional) { body } // 3

[ captures ] < tparams > requires(optional) { body } // 4
[ captures ] < tparams > requires(optional) specs { body } // 4
```
1. Full form
2. Omitted parameter list: function takes no arguments, as if the parameter list were `()`.
3) Same as 1), but specifies a generic lambda and explicitly provides a list of template parameters.
4) Same as 2), but specifies a generic lambda and explicitly provides a list of template parameters.

>[!INFO]- More info...
> `captures`	- a comma-separated list of zero or more captures, optionally beginning with a capture-default.
>>[!INFO|clean collapse no-i ttl-c]- See below for the detailed description of captures
>> A lambda expression can use a variable without capturing it if the variable
>>- \- is a non-local variable or has static or thread local storage duration (in which case the variable cannot be captured), or
>>- \- is a reference that has been initialized with a constant expression.
>> 
>> A lambda expression can read the value of a variable without capturing it if the variable
>>- \- has const non-volatile integral or enumeration type and has been initialized with a constant expression, or
>>- \- is constexpr and has no mutable members.
>
> <br>
> 
> `tparams` - a non-empty comma-separated list of template parameters, used to provide names to the template parameters of a generic lambda (see `ClosureType::operator()` below).
>
> <br>
> 
> `params`	- The list of parameters, as in named [[C++functions|`functions`]].
>
> <br>
> 
> `specs` - consists of `specifiers`, `exception`, `attr` and `trailing-return-type` in that order; each of these components is optional
>
> <br>
> 
> `specifiers`	-	Optional sequence of specifiers. If not provided, the objects captured by copy are `const` in the lambda body. 
>>[!INFO|clean ttl-c collapse no-i]- The following specifiers are allowed at most once in each sequence:
>>- **mutable**: allows body to modify the objects captured by copy, and to call their non-const member functions
>>- 
>>- **constexpr**: explicitly specifies that the function call operator or any given operator template specialization is a constexpr function. When this specifier is not present, the function call operator or any given operator template specialization will be constexpr anyway, if it happens to satisfy all constexpr function requirements *(since C++17)*
>>- 
>>- **consteval**: specifies that the function call operator or any given operator template specialization is an immediate function. `consteval` and `constexpr` cannot be used at the same time. *(since C++20)*
>>- 
>>- **static**: specifies that the function call operator or any given operator template specialization is a static member function. `mutable` and `static` cannot be used at the same time, and captures must be empty if `static` is present. *(since C++23)*
>
> <br>
> 
> `exception` -	provides the dynamic exception specification or *(until C++20)* the `noexcept` specifier for `operator()` of the closure type
>
> <br>
> 
> `attr`	-	provides the attribute specification for the type of the function call operator or operator template of the closure type. Any attribute so specified does not appertain to the function call operator or operator template itself, but its type. (For example, the `noreturn` attribute cannot be used.)
>
> <br>
> 
> `trailing-return-type` -	-> `ret`, where `ret` specifies the return type. If trailing-return-type is not present, the return type of the closure's `operator()` is deduced from return statements as if for a function whose return type is declared auto.
>
> <br>
> 
> `requires` - *(since C++20)* adds constraints to `operator()` of the closure type
>
> <br>
> 
> `body`	-	Function body

**Declaring and Initializing Lambda function**
```cpp
#include <iostream>

int main(int argc, char **argv)
{
    auto func = [](){ 
	    std::cout << "Hello World!";
    };

    func();
    return 0;
}
```

**Labmda function w/out name**
```cpp
#include <iostream>

int main(int argc, char **argv)
{
    [](){
        std::cout << "Hello World!";
    }();

    return 0;
}
```
>[!column|no-t collapse]
>>[!INFO|clean no-i ttl-c] [[C++functionslambda1|Sample 1]]
>
>>[!INFO|clean no-i ttl-c] [[C++functionslambda2|Sample 2]]
>
>>[!INFO|clean no-i ttl-c] [[C++functionslambda3|Sample 3]]

<br>

# 
---
**Sources:**
- https://en.cppreference.com/w/cpp/language/lambda