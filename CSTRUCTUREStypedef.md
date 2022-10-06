#C #Clecture #Cstructures #Ctypedef
# Typedef Keyword
> Syntax: `typedef existing_data_type new_data_type`

`typedef` gives freedom to the user by allowing them to create their own types.
```C
typedef int INTEGER;

int main(){
	INTEGER var=100;
	printf("%d", var); //100

	return 0;
}
```

### Use of `typedef` in structures
```C
typedef struct{
	char engine[50];
	char *fuelType;
}car;

int main(){
	car c1;
}
```

<br>

# 
---
**[BACK](Cstructures)**
**Source:**
- [Structure Types (Using typedef) - YouTube](https://www.youtube.com/watch?v=Bw3sUC6Txus&list=PLBlnK6fEyqRhX6r2uhhlubuF5QextdCSM&index=153)