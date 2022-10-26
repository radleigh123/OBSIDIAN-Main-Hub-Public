---
aliases:
---
**tags:** #C/stdio/scanf #C/Strings #C/Lecture 
**[[C_IMPORTANT#^b4fc22|BACK]]**

---
## Accepting strings with space
```C
// Using fgets() function
#define MAX_LIMIT 20

char str[MAX_LIMIT];
fgets(str, MAX_LIMIT, stdin);
printf("%s", str);
```
```C
/* ^\n tells to take input until newline doesn’t get encountered. Then, with this %*c, it reads newline character and here used * indicates that this newline character is discarded.
*/
char str[20];
scanf("%[^\n]%*c", str);
printf("%s", str);
```
```C
/* ^\n tells to take input until newline doesn’t get encountered. Here we used ^ (XOR -Operator ) which gives true until both characters are different. Once the character is equal to New-line (‘\n’),  ^ (XOR Operator ) gives false to read the string. So we use “%[^\n]s” instead of “%s”.
*/
char str[100];
scanf("%[^\n]s",str);
printf("%s",str);
```

# 

<br>

---
**Sources:**
- [Taking String input with space in C (4 Different Methods) - GeeksforGeeks](https://www.geeksforgeeks.org/taking-string-input-space-c-3-different-methods/#:~:text=So%20to%20get%20a%20line,n%5Ds%E2%80%9D%2Cstr)%3B)