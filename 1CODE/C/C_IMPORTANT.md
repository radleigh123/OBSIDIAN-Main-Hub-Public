#programming 
- It is the job of preprocessor (not compiler) to <mark class="hltr-blue">replace Macros with their corresponding values.</mark>
```C
#define STRING "%s \n"
#define NESO "Hello World!"
int main()
{
	printf(STRING, NESO); // Hello World!
	return 0;
}
```
- <mark class="hltr-blue">1st printf function</mark> will read how many characters lies in<mark class="hltr-blue"> 2nd printf function</mark>.
```C
printf("Total chars: %d", printf("66\t")); 
//66 Total chars: 3
// 2nd printf has to be executed first, before 1st printf can get the value out of it
```

---
**[MAINHUB C](mainC)**