---
cssclass: no-m
aliases:
- conversion
- type casting
tags:
- C/Typecasting
---
**[[C|HOME [C]]]**

---
## Typecasting
allows us to convert one data type into other. In C language, we use cast operator for typecasting which is denoted by (type).
>[!EXAMPLE|alt-co collapse no-i] **Syntax:** `(type) value;`
>- 
>
>>[!WARNING|txt-c ttl-c]+ 
>> It is always recommended to convert the lower value to higher for avoiding data loss.
```C
#include<stdio.h>  
int main(){  
	double num = (double)9/4;    
	printf("num: %lf", num); // 2.25000
	
	return 0;  
}
```
# 

<br>

---
**Sources:**
- [Type Casting in C - javatpoint](https://www.javatpoint.com/type-casting-in-c)