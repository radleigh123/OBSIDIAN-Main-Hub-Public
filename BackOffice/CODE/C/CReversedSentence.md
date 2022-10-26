---
aliases:
---
**tags:** #C/Strings/Loops #C/Functions/Recursion #C/Functions/Void  
**[[1Strings|BACK]]**

---
```C
#include<stdio.h>

void reversedSentence();

int main(){
    printf("Enter a sentence: ");
    reversedSentence();

    return 0;
}

void reversedSentence(){
    char char1;
    scanf("%c", &char1);

    if (char1 != '\n'){
        reversedSentence(); // recursion function 
        printf("%c", char1);
    }
}
```