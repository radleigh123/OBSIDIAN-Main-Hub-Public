---
aliases:
---
**tags:** #C/Structures/Tags #C/Structures/Packing  #C/Lecture 
**[[Cstructures|BACK]]**

---
## Structure Packing
> Because of structure padding, size of the structure becomes more than the size of the actual structure. Due to this some memory will get wasted.
> > We can avoid the wastage of memory by simply writing [**`#pragma pack(1)`**](Cpragma.md)

```C
#pragma pack(1)

struct abc {
	char a;
	int b;
	char c;
} var;

int main(){
	printf("%d", sizeof(var)); // 6
	return 0;
}
```

# 

<br>

---
**Source:**
[(81) Structure Packing in C - YouTube](https://www.youtube.com/watch?v=VZBLCpQYchs&list=PLBlnK6fEyqRhX6r2uhhlubuF5QextdCSM&index=159)