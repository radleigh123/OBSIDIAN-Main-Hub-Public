#C #Clecture #Cstructures #Cstructuretags #Carrays #Carraystructure
# Declaring an array of structure
> Instead of declaring multiple variables, we can also declare an array of structure in which element of the array will represent a structure variable.

```C
#include <stdio.h>

typedef struct
{
    int age;
} person;

int main()
{
    person p[2];
    for (int i = 0; i < 2; i++)
    {
        printf("Enter age: ");
        scanf("%d", &p[i].age);
    }
    
    for (int i = 0; i < 2; i++)
    {
        printf("Age: %d\n", p[i].age);
    }

    return 0;
}
```

<br>

# 
---
**[BACK](Cstructures)**
**Sources:**
- [Declaring an Array of Structure - YouTube](https://www.youtube.com/watch?v=EGeIsvx4Wns&list=PLBlnK6fEyqRhX6r2uhhlubuF5QextdCSM&index=156)