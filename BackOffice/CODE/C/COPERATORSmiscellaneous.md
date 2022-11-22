---
aliases:
tags:
- C/Operators
- C/Lecture
---
**[[C|HOME [C]]]**

---
## Miscellaneous operators
**Comma operator `,`**
- used as a separator
- returns the rightmost operand in expression, it simply evaluates the rest of the operands and rejects them.

```C
#include<stdio.h>
int main() {
	int a = 0, b = (a++, 3, 8);

	printf("%d\n", a); // 1
	printf("%d", b); // 8
	return 0;
}
```
>[!column|flex no-t]
>>[!EXAMPLE|no-i ttl-c]  Sample 1
>>```C
>>	int a;
>>	a = 3, 4, 8; // (a = 3), 4, 8
>>	
>>	printf("%d", a); // 3
>>```
>
>>[!EXAMPLE|no-i ttl-c] Sample2
>> ```C
>> 	int a = 3, 4, 8 // int a =3, int 4, int 8
>> 
>> 	printf("%d", a); // ERROR!
>> ```

---
**Pointer operator `*`**
used to define pointer variables in C

---
**Dot operator `.`**
used to access members of [[Cstructures|structures]] or [[Cunions|unions]].