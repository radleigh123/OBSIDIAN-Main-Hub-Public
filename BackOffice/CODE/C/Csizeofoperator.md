---
aliases:
tags:
- C/Lecture
- C/Operators
---
**[[C|HOME [C]]]**

---
## `sizeof()` Operator
determines the size of the expression or the data type specified in the number of char-sized storage units. The `sizeof()` operator behaves differently according to the type of the operand.

**When [[COPERATORSarithmetic|operand]] is a data type**
```C
#include <stdio.h>  
int main()  
{  
    int x=89; // variable declaration

    printf("size of the variable x is %d", sizeof(x));

    printf("\nsize of the integer data type is %d",sizeof(int));
    printf("\nsize of the character data type is %d",sizeof(char));
    printf("\nsize of the floating data type is %d",sizeof(float));
    
    return 0;
}
```
**When [[COPERATORSarithmetic|operand]] is an expression**
```C
#include <stdio.h>
int main()
{
  double i=78.0; //variable initialization
  float j=6.78; //variable initialization
  
  printf("size of (i+j) expression is : %d",sizeof(i+j)); // 8
  //Displaying the size of the expression (i+j).
  return 0;
}
```

<br>

# 
---
**Sources:**
- [sizeof() operator in C - javatpoint](https://www.javatpoint.com/size-of-operator-in-c)