#C #Clecture #Cstatic

Any assignment are not allowed on outside the function block (`{}`)

```C
static int i = 27;
static int i; // **declaring only**, not defining
i = 45; // error **redefinition**, this is an *ASSIGNMENT*

int main(){
	static int i;
	printf("%d", i); / 0

	i = 45;
	printf("%d", i); / 45
	return 0;
}
```

---
**[[C_IMPORTANT]]**