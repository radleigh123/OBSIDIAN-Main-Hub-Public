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