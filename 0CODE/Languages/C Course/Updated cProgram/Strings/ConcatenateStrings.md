```C
// Concatenating two strings without using STRCAT
#include<stdio.h>

int main(){
    char str1[100] = "programming ", str2[100] = "is awesome";
    int length;

    // store length of str1 in the length variable
    length = 0;
    while (str1[length] != '\0'){
        length++;
    }
    
    // concatenates str2 to str1
    for (int i = 0; str2[i] != '\0'; i++, length++){
        str1[length] = str2[i];
    }
    
    // terminating the str1 string
    str1[length] = '\0';

    printf("After concatenation: ");
    puts(str1);

    return 0;
}
```