**[C](C#^STRUCT)**

#C #Clecture #Cstructures 
# Structures
- is a user defined data type that can be used to group elements of different types into a single type.
```C
struct{
	char *engine;
} car1, car2;

int main(){
	car1.engine = "DDis 190 Engine";
	car2.engine = "1.0 L Kappa Dual VTVT";
	
	printf("%s\n%s", car1.engine, car2.engine);
	return 0;
}
```

>[!INFO]- ### Initializing Structure members
| ![[Pasted image 20221006171554.png]] | ![[Pasted image 20221006171620.png]] |
| ------------------------------------ | ------------------------------------ |

>[!CITE] **See also:**
>1.  [Structure Tags](CSTRUCTUREStypes.md)
>2.  [Typedef Keyword](CSTRUCTUREStypedef.md)
>3.  [Designated Initialization](CSTRUCTURESdesignateinitial.md)
>4.  [Declare an array of structures](CSTRUCTURESarraystructure.md)
>5. [Accessing members of structure using structure pointer](CSTRUCTURESpointerstructure.md)
>6. [Structure Padding](CSTRUCTUREpadding.md)
>7. [Structure Packing](CSTRUCTUREpacking.md)

<br>

# 
---
**Sources:**
- [Declaring Structure Variables - YouTube](https://www.youtube.com/watch?v=3pFSbSVIwKU&list=PLBlnK6fEyqRhX6r2uhhlubuF5QextdCSM&index=151)
- [Initializing & Accessing the Structure Members - YouTube](https://www.youtube.com/watch?v=2DidKZmwNMo&list=PLBlnK6fEyqRhX6r2uhhlubuF5QextdCSM&index=154)