---
aliases:
tags:
- C/Operators
- C/Lecture
---
**[[C|HOME [C]]]**

---
## Unary Operators
**Increment & Decrement Operators**
- are [[COPERATORSunary|unary operators]], applied on a single operand.
>[!column|flex no-t]
>>[!NOTE|clean no-t ttl-c txt-c collapse] Increment
>> pre-increment: **`++a`**
>> post-increment: **`a++`**
>
>>[!NOTE|clean no-t ttl-c txt-c collapse] Decrement
>> pre-decrement: **`--a`**
>> post-decrement: **`a--`**

>[!WARNING]- You cannot use **[rvalue](Cleftrightvalue.md)** before or after increment/decrement operator
> ```C
> (a + b)++; // error!
> ++(a + b); // error!
> 
> // (a+b)++ equivalent to (a+b) = (a+b) + 1;
> ```
> 
> ![[Pasted image 20221007150335.png|cover center hs-med]]