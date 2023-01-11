---
cssclass: no-m
title: Cgoto
creation-date: 2022-11-05
aliases:
tags:
- C
---
**[[C|HOME [C]]]**

---
# `goto` statement (depreciated)
is known as jump statement in C
```C
#include <stdio.h>

int main()
{
    int num,i=1;

    printf("Enter the number whose table you want to print?");
    scanf("%d",&num);

    table:
    printf("%d x %d = %d\n",num,i,num*i);
    
    i++;
    if(i<=10) goto table;

    return 0;
}
```

<br>

# 
---
**Sources:** 
- [C goto statement - javatpoint](https://www.javatpoint.com/c-goto)