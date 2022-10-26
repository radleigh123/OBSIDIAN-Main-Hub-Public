---
aliases:
---
**tags:** #C/Strings #C/Miscellaneous/macros 
**[[0Additional Topics]]**

---
## CMacrodate
```C
// a string containing the current date

#include<stdio.h>
int main(){
    printf("Current Date: %s", __DATE__);
}
```