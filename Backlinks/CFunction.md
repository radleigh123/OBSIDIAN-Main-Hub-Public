#C #Cfunctions #Creturnfunction

```C
#include<stdio.h>

int addNumbers(int, int);

int main(){
    int n3, n4, result;
    printf("Enter two integers: ");
    scanf("%d%d", &n3, &n4);

    // return value is stored in result
    result = addNumbers(n3, n4);
    printf("Sum = %d", result);

    return 0;
}

int addNumbers(int n1, int n2){
    int sum;
    sum = n1 + n2;
    
    return sum;
}
```