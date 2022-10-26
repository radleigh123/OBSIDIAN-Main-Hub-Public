---
aliases:
---
**tags:** #C/Strings #C/Miscellaneous/macros #C/Preprocessor_Directive #C/Lecture  
**[[C_IMPORTANT#^05afd0|BACK]]**

---
It is the job of preprocessor (not compiler) to <mark class="hltr-blue">replace Macros with their corresponding values.</mark>

```C
#define STRING "%s \n"
#define NESO "Hello World!"
int main()
{
	printf(STRING, NESO); // Hello World!
	return 0;
}
```