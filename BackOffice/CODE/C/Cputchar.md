---
aliases:
---
**tags:** #C/stdio/putchar #C/Lecture 
**[[Cstdioh|BACK]]**

---
## `putchar()` function
> accepts an integer argument (which represents a character it wants to display) and return an integer representing the character written on the screen.
> >Prototype:  `int putchar(int ch)`
> >- <mark class="hltr-lightred">CHARACTER IS INTERNALLY REPRESENTED IN BINARY FORM ONLY</mark>  EX. <u>**A = 65 (ASCII Code)**</u>
> >- IT DOESN'T MAKE ANY DIFFERENCE IF YOU WRITE `int ch` instead of `char ch`.

```C
// program to print A to Z
	int ch;
    for (ch = 'A'; ch <= 'Z'; ch++)
    {
        putchar(ch);
    }
```