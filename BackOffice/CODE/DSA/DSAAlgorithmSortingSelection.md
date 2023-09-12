---
cssclasses:
- hide-header-underline-1
aliases: []
tags:
- DSA/Algorithm/Sorting 
---
**[[DSAAlgorithmSorting|BACK]]**

---
## Selection Sort
a simple and efficient sorting algorithm that works by repeatedly selecting the smallest (or largest) element from the unsorted portion of the list and moving it to the sorted portion of the list.
>[!CHECK]- How it works
> ```java
> int arr[] = {64, 25, 12, 22, 11};
> ```
> 
>>[!grid]
>> ![[DSAAlgorithmSortingSelection1.png| center hsmall]]
>> ![[DSAAlgorithmSortingSelection2.png| center hsmall]]
>> 
>> ![[DSAAlgorithmSortingSelection3.png| center hsmall]]
>> ![[DSAAlgorithmSortingSelection4.png| center hsmall]]
>> 
>> ![[DSAAlgorithmSortingSelection5.png| center hsmall]]

>[!aside|right]-
> ```
> 11 12 22 25 64 
> ```

```java
int[] arr = { 64, 25, 12, 22, 11 };

int n = arr.length;
 
// One by one move boundary of unsorted subarray
for (int i = 0; i < n-1; i++)
{
	// Find the minimum element in unsorted array
	int min_idx = i;
	for (int j = i+1; j < n; j++)
		if (arr[j] < arr[min_idx])
			min_idx = j;

	// Swap the found minimum element with the first
	// element
	int temp = arr[min_idx];
	arr[min_idx] = arr[i];
	arr[i] = temp;
}
```

**Slightly improved Selection sort**
```java
static void minMaxSelectionSort(int[] arr)
{
	int n = arr.lenght;

	for (int i = 0, j = n - 1; i < j; i++, j--) {
		int min = arr[i], max = arr[i];
		int min_i = i, max_i = i;
		
		for (int k = i; k <= j; k++) {
			if (arr[k] > max) {
				max = arr[k];
				max_i = k;
			} else if (arr[k] < min) {
				min = arr[k];
				min_i = k;
			}
		}

		// shifting the min.
		swap(arr, i, min_i);

		// Shifting the max. The equal condition
		// happens if we shifted the max to arr[min_i]
		// in the previous swap.
		if (arr[min_i] == max) {
			swap(arr, j, min_i);
		} else {
			swap(arr, j, max_i);
		}
	}
}

static int[] swap(int []arr, int i, int j)
{
	int temp = arr[i];
	arr[i] = arr[j];
	arr[j] = temp;
	return arr;
}
```

<br>

# 
---
- [Selection Sort – GeeksforGeeks](https://www.geeksforgeeks.org/selection-sort/)
	- [A sorting algorithm that slightly improves on selection sort](https://www.geeksforgeeks.org/sorting-algorithm-slightly-improves-selection-sort/?ref=lbp)