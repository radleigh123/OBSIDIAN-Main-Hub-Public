---
aliases:
tags:
- C/Variables
---
**[[Cvariables#Types of Variables in C|BACK]]**

---
## Automatic Variable
All variables in C that are declared inside the block, are automatic variables by default. We can explicitly declare an automatic variable using **auto keyword**.
```C
void main(){
	int num1 = 10; //local variable (or automatic)
	auto int num2 = 20; //automatic variable
}
```