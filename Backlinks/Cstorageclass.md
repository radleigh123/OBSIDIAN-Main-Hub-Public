#C #Clecture #Cstorageclass

> A storage class defines the scope (visibility) and life-time of variables and functions within a C Program. These features basically include the scope, visibility and life-time which help us to trace the existence of a particular variable during the runtime of a program.
> **Syntax:** `storage_class var_dataType var_name;`

### auto
- is the default storage class for all local variables
- assigned a garbage value (random) by default whenever they are declared.
```C
{
	int var;
	auto int var; // both are equivalent
}
```

### register
-   is used to define local variables that should be stored in a register instead of RAM.
-   is that the compiler tries to store these variables in the register of the microprocessor if a free registration is available.
-   we cannot obtain the address of a register variable using pointers.
```C
{
	register int miles;
}
```

### extern
-   simply tells us that the variable is defined elsewhere and not within the same block where it is used.
-   most commonly used when there are two or more files sharing the same global variables or functions.
```C
int count; // MAIN FILE
extern void writeExtern();

int main(){
	count = 5;
	writeExtern(); // Count is 5
}
```
```C
extern int count; // SUPPORT FILE

void writeExtern(){
	printf("Count is %d", count);
}
```

### static
-   instructs the compiler to keep a local variable in existence during the life-time of the program instead of creating and destroying it each time it comes into and goes out of scope.
-   is used on a global variable, it causes only one copy of that member to be shared by all the objects of its class.
```C
#include <stdio.h>
 
/* function declaration */
void func(void);
 
static int count = 5; /* global variable */
 
main() {
   while(count--) {
      func();
   }
   return 0;
}

/* function definition */
void func( void ) {
   static int i = 5; /* local static variable */
   i++;
   printf("i is %d and count is %d\n", i, count);
}

/* results
i is 6 and count is 4
i is 7 and count is 3
i is 8 and count is 2
i is 9 and count is 1
i is 10 and count is 0 */
```

<br>

# 
---
**[[C]]**
**Sources:**
- [Storage Classes](https://www.tutorialspoint.com/cprogramming/c_storage_classes.htm)
- [Storage GeeksforGeeks](https://www.geeksforgeeks.org/storage-classes-in-c/)