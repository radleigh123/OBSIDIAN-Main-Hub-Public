---
aliases:
---
**tags:** #C/Unions #C/Structures 
**[[CCODES|BACK]]**

---
### Union
```C
// Structures allocate enough space to store all their members, 
// whereas unions can only hold one member value at a time.
#include<stdio.h>
union Onion{
    char name[32];
    double salary;
} onion;

struct Structure{
    char name[32];
    double salary;
} structure;

int main(){
    printf("Size of Union: %d bytes\n", sizeof(onion)); // 32 bytes
    // It's because the size of a union variable,
    // will always be the size of its largest element. Largest element is name[32]

    printf("Size of Structure: %d bytes", sizeof(structure)); // 40 bytes
    // 32 bytes + 8 bytes

    return 0;
}
```

### Accessing Unions
```C
#include<stdio.h>
union Job{
    float salary;
    int worker;
} job;

int main(){
    job.salary = 12.66;

    // when j.worker is assigned a Value
    // j.salary will No longer hold 12.66
    job.worker = 22;

    printf("Salary: %.2f\n", job.salary);
    printf("Worker: %d", job.worker);

    return 0;
}
```