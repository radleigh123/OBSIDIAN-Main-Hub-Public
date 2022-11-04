---
cssclass: no-m
aliases:
tags:
- C/File_Handling 
---
**[[Cfilehandling|BACK]]**

---
>[!recite|collapse no-i] Delete a file
```C
#include <stdio.h>

int main() {
    remove("proto2.txt"); // Must be from the same directory

    return 0;
}
```

>[!recite|no-i collapse] Renaming a file
```C
#include <stdio.h>

int main() {
    rename("protobin.bin", "proto.bin");

    return 0;
}
```
# 

<br>

---
**Sources:**
- [How to Delete a file using c program | by Sanjay Gupta - YouTube](https://www.youtube.com/watch?v=BZR1CUCPWFI&list=PL-gW8Fj5TGrpVCun29h8HqtysUq6OPq3X&index=29)