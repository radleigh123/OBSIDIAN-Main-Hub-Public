---
aliases:
---
**tags:** #C/Pointers #C/Lecture 
**[[C_IMPORTANT#^b7a0f2|BACK]]**

---
## Segmentation Fault
- caused by the program trying to read/write an illegal memory location.
```C
int *ptr;
*ptr = 1; // very illegal
```