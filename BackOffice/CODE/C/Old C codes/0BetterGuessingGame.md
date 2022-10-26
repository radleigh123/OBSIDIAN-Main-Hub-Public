---
aliases:
---
**tags:** #C/Loop  
**[[CCODES|BACK]]**

---
## Better Guessing Game
```C
#include<stdio.h>

int main(){
    int guessNumber, secretNumber = 5;
    int limit = 3;

    printf("Guess the number:\n");
    while (guessNumber != secretNumber && !(limit == 0)){
        if (limit == 1){
            printf("%d guess remaining:\n", limit);
        } else{
            printf("%d guesses remaining:\n", limit);
        }
        printf("    -> ");
        scanf("%d", &guessNumber);

        // loop breaks until limit = 0
        limit--;
    }
    
    if (guessNumber != secretNumber){
        printf("\nGame over!");
    } else{
        printf("\nCongratulations!!!");
    }

    return 0;
}
```