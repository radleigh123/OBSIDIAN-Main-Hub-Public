---
aliases:
tags:
- C/Variables
---
**[[Cvariables#Types of Variables in C|BACK]]**

---
## Static Variables
A variable that is declared with the static keyword is called static variable.
It retains its value between multiple function calls.
```C
void function1(){
	int num1 = 10; //local variable
	static int num2 = 10; //static variable

	num1 += 1;
	num2 += 1;
	printf("%d, %d", num1, num2);
	
	/* If you call this function many times, the local variable will print
	the same value for each function call, e.g, 11,11,11 and so on. But the
	static variable will print the incremented value in each function call,
	e.g.11, 12, 13 and so on. */
}
```