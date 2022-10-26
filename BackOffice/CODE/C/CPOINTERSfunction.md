---
aliases:
---
**tags:** #C/Pointers/Functions #C/Lecture #C/Functions 
**[[Cpointers#^459955|BACK]]**

---
## Pointer functions
> are like normal pointers but they have the capability to point to a function.

#### How to declare a pointer to an array
**`int *ptr[10];`** is <mark class="hltr-lightred">not recommended</mark>. 
- Precedence of **`[]`** is higher than **`*`**
- Hence, `ptr` is an array of 10 pointers pointing to integers.

**`int (*ptr)[10];`** <mark class="hltr-lightgreen">solution</mark>
- Hence, `ptr` is pointing to an array of 10 integers.

#### How to declare a pointer to a function
```C
int add(int a, int b){
	return a + b;
}

int main(){
	int (*ptr)(int, int);
	// ptr is a pointer which is pointing to a function containing two integer arguments and it returns an integer
}
```

#### Assigning the address of a function to a function pointer
```C
int main(){
	int (*ptr)(int, int) = &add;
}

/* -------------------------------------------------------------------------------*/

int main(){
	int (*ptr)(int, int);
	ptr = &add;
}
```

#### Using the function pointer
```C
int result;
int (*ptr)(int, int) = &add;

result = *ptr(10, 20);
printf("%d", result);

/* -------------------------------------------------------------------------------*/

int result;
int (*ptr)(int, int) = add; // name of the function represents the initial address of that function

result = ptr(10, 20);
printf("%d", result);
```

### Function pointers application
Call a function at a certain point in time
```C
int func(int a, int b){
	return a + b;
}

int main(){
	printf("%d", func(2, 5));
	return 0;
}
```
**[Designing a calculator using Pointer functions](CPOINTERcallfunctionpointers.md)** ^2500ed

<br>

# 
---
**Source:**
- [Function Pointers in C - YouTube](https://www.youtube.com/watch?v=BRsv3ZXoHto&list=PLBlnK6fEyqRhX6r2uhhlubuF5QextdCSM&index=151)
- [Application of Function Pointers in C - YouTube](https://www.youtube.com/watch?v=wQ-gWwKKeP4&list=PLBlnK6fEyqRhX6r2uhhlubuF5QextdCSM&index=150)