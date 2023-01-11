---
aliases:
tags:
- C/Lecture
- C/Arrays/Boolean
- C/Typedef
---
**[[C|HOME [C]]]**

---
## Boolean
> is a data type that contains two types of values, i.e., 0 and 1
> **Syntax:** `bool variable_name;` 

### Boolean [[Carrays|array]]
>[!aside|show-title] **Output**
> 0 1 0 1 0 1 0 1 0 1 0 1
```C
#include<stdio.h>  
#include<stdbool.h>  
int main()  
{  
    int count;
	bool b[2]={false,true}; // Boolean type array
	
	for(int i = 0; i < 5; i++) {  
		for (int j = 0; j < 2; j++)
        {
            printf("%d ", b[j]);
        }
	}
	
	return 0;
}
```

### Boolean [[CSTRUCTUREStypedef|typedef]]
>[!aside|show-title] **Output**
> The value of x is FALSE, 1
```C
#include<stdio.h>
typedef enum{true, false} b;

int main()
{
    b x = false; // variable initialization
    
    if (x == true) printf("The value of x is TRUE, %d", x);
    else printf("The value of x is FALSE, %d", x); // 1 = `false` is a 2nd array element

    return 0;
}
```


<br>

# 
---
**Sources**
- [C Boolean - javatpoint](https://www.javatpoint.com/c-boolean)