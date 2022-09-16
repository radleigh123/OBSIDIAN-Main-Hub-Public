```C
// Program to copy strings without using STRCPY
#include<stdio.h>

int main(){
    char str1[100], str2[100], i;
    printf("Enter string str1: ");
    fgets(str1, sizeof(str1), stdin);

    for (i = 0; i < str1[i] != '\0'; i++){
        str2[i] = str1[i];
    }
    
    str2[i] = '\0';
    printf("String str2: %s", str2);
    
    return 0;
}
```