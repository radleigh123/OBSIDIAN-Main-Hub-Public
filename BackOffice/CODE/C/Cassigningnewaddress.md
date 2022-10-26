---
aliases:
---
**tags:** #C/Arrays #C/Arrays/Pointers #C/Arrays/2D #C/Lecture 
**[[C_IMPORTANT#^ae460a|BACK]]**

---
![[Pasted image 20221007143415.png|650]]


<mark class="hltr-lightgreen">Correct solution:</mark>
```C
int a[] = {1, 2, 3};
int *ptr = a;

printf("%d", *(++ptr)); // 2
```