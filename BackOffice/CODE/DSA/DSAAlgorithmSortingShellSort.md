---
cssclasses:
- hide-header-underline-2
- hide-header-underline-5
aliases: []
tags:
- DSA/Algorithm/Sorting 
---
**[[DSAAlgorithmSorting|BACK]]**

---
## ShellSort
> mainly a variation of [[DSAAlgorithmSortingInsertion|Insertion Sort]]

The idea of ShellSort is to allow the exchange of far items. In Shell sort, we make the array h-sorted for a large value of h. We keep reducing the value of h until it becomes 1. An array is said to be h-sorted if all sublists of every h’th element are sorted.
>[!CITE|no-i ttl-c color-black]- How it works
>
> Algorithms:
> ```
>  1  START
>  2  Initialize the value of gap size. Example: `h`
>  3  Divide the list into smaller sub-part. Each must have equal intervals to `h`
>  4  Sort these sub-lists using insertion sort
>  5  Repeat this step 2 until the list is sorted.
>  6  Print a sorted list.
>  7  STOP
> ```
> &nbsp;
> Pseudocode:
> ```
> PROCEDURE SHELL_SORT(ARRAY, N)  
> 	WHILE GAP < LENGTH(ARRAY) /3 :
> 		GAP = ( INTERVAL * 3 ) + 1
> 	END WHILE LOOP
> 	
> 	WHILE GAP > 0 :
> 		FOR (OUTER = GAP; OUTER < LENGTH(ARRAY); OUTER++):
> 			INSERTION_VALUE = ARRAY[OUTER]
> 			INNER = OUTER;
> 			
> 			WHILE INNER > GAP-1 AND ARRAY[INNER – GAP] >= INSERTION_VALUE:
> 				ARRAY[INNER] = ARRAY[INNER – GAP]
> 				INNER = INNER – GAP
> 			END WHILE LOOP
> 			
> 			ARRAY[INNER] = INSERTION_VALUE
> 		END FOR LOOP
> 		
> 		GAP = (GAP -1) /3;
> 	END WHILE LOOP
> 	
> END SHELL_SORT
> ```

>[!aside|right]-
> ```
> 2 3 12 34 54 
> ```

```java
int arr[] = { 12, 34, 54, 2, 3 };

int sort(int arr[])
{
	int n = arr.length;

	// Start with a big gap, then reduce the gap
	for (int gap = n/2; gap > 0; gap /= 2)
	{
		// Do a gapped insertion sort for this gap size.
		// The first gap elements a[0..gap-1] are already
		// in gapped order keep adding one more element
		// until the entire array is gap sorted
		for (int i = gap; i < n; i += 1)
		{
			// add a[i] to the elements that have been gap
			// sorted save a[i] in temp and make a hole at
			// position i
			int temp = arr[i];

			// shift earlier gap-sorted elements up until
			// the correct location for a[i] is found
			int j;
			for (j = i; j >= gap && arr[j - gap] > temp; j -= gap)
				arr[j] = arr[j - gap];

			// put temp (the original a[i]) in its correct
			// location
			arr[j] = temp;
		}
	}
	return 0;
}
```

**Alternative**
```java
int[] arr = { 12, 11, 13, 5, 6 };

int n = arr.length;

for (int gap = n / 2; gap > 0; gap /= 2)
{
	for (int i = gap; i < n; ++i) {
		int j = i;
	
		while (j >= gap && arr[j] < arr[j - gap])
		{
			int temp = arr[j];
			arr[j] = arr[j - gap];
			arr[j - gap] = temp;
			j -= gap;
		}
	}
}
```

<br>

# 
---
- [ShellSort - GeeksforGeeks](https://www.geeksforgeeks.org/shellsort/)
- [ShellSort using Streams | Geekific - YouTube](https://www.youtube.com/watch?v=IViqgakt-Eg)