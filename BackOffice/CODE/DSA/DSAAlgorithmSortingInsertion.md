---
cssclasses:
- hide-header-underline-2
aliases: []
tags:
- DSA/Algorithm/Sorting 
---
**[[DSAAlgorithmSorting|BACK]]**

---
## Insertion Sort
> *works similar to the way you sort playing cards in your hands*

The array is virtually split into a sorted and an unsorted part. Values from the unsorted part are picked and placed at the correct position in the sorted part.

![[DSAAlgorithmSortingInsertion1.png|center ws-med]]

>[!aside|right]-
> ```
> 5 6 11 12 13
> ```

```java
int[] arr = { 12, 11, 13, 5, 6 };

int n = arr.length;

for (int i = 1; i < n; ++i)
{
	int key = arr[i];
	int j = i - 1;

	/* Move elements of arr[0..i-1], that are
	   greater than key, to one position ahead
	   of their current position */
	while (j >= 0 && arr[j] > key)
	{
		arr[j + 1] = arr[j];
		j = j - 1;
	}
	arr[j + 1] = key;
}
```

**Alternative**
```java
int[] arr = { 12, 11, 13, 5, 6 };

int n = arr.length;

for (int i = 1; i < n; ++i)
{
	int j = i;

	while (j > 0 && arr[j] < arr[j - 1])
	{
		int temp = arr[j];
		arr[j] = arr[j - 1];
		arr[j - 1] = temp;
		j--;
	}
}
```

<br>

# 
---
- [Insertion Sort - GeeksforGeeks](https://www.geeksforgeeks.org/insertion-sort/)