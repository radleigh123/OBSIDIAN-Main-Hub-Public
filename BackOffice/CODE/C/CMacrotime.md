---
aliases:
---
**tags:** #C/Strings #C/Miscellaneous/macros 
**[[0Additional Topics|BACK]]**

---
## CMacrotime
```C
// a string containing the current time

#include<stdio.h>
int main(){
    printf("Current Time: %s", __TIME__);
}
```