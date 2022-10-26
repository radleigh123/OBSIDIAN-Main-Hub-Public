---
aliases:
---
**tags:** #C/Operators #C/Lecture
**[[C_IMPORTANT#^421c7b|BACK]]**

---
**C standard** is the language specification which is adopted by all C compilers across the globe.

![Untitled](Untitled%201.png)
    
- Therefore, `**i++`** inside `sizeof` is not evaluated.
```C
int = 5;
int var = sizeof(i++);
printf("%d %d", i, var); // 5  4
```