---
cssclasses:
- hide-header-underline-2
aliases: []
tags:
- DSA/Algorithm/Sorting 
---
**[[DSAAlgorithmSorting|BACK]]**

---
## QuickSort
> based on the [[DSAAlgorithmDivideConquer|Divide and Conquer algorithm]]

picks an element as a pivot and partitions the given array around the picked pivot by placing the pivot in its correct position in the sorted array.

Choice of Pivots:
$\quad$◾ Always pick the first element as a pivot.
$\quad$◾ Always pick the last element as a pivot (implemented below)
$\quad$◾ Pick a random element as a pivot.
$\quad$◾ Pick the middle as the pivot.

>[!CITE|color-black no-i]- How it works?
> The key process in **QuickSort** is the `partition()`. The target of partitions is to place the pivot (any element can be chosen to be a pivot) at its correct position in the sorted array and put all smaller elements to the left of the pivot, and all greater elements to the right of the pivot.
> 
> Partition is done recursively on each side of the pivot after the pivot is placed in its correct position and this finally sorts the array.
> 
> ![[DSAAlgorithmSortingQuickSort.png|center]]
> 
>>[!grid]
>> ![[DSAAlgorithmSortingQuickSort2.png| hmed]]
>> ![[DSAAlgorithmSortingQuickSort3.png| hmed]]
>> 
>> ![[DSAAlgorithmSortingQuickSort4.png| hmed]]
>> ![[DSAAlgorithmSortingQuickSort5.png| hmed]]
>> 
>> ![[DSAAlgorithmSortingQuickSort6.png| hm-sm]]

>[!aside|right]-
> ```
> 1 5 7 8 9 10 
> ```

```java
int[] arr = { 10, 7, 8, 9, 1, 5 };

// The main function that implements QuickSort
// arr[] --> Array to be sorted,
// low --> Starting index,
// high --> Ending index
static void quickSort(int[] arr, int low, int high)
{
	if (low < high) {

		// pi is partitioning index, arr[p]
		// is now at right place
		int pi = partition(arr, low, high);

		// Separately sort elements before
		// partition and after partition
		quickSort(arr, low, pi - 1);
		quickSort(arr, pi + 1, high);
	}
}

// This function takes last element as pivot,
// places the pivot element at its correct position
// in sorted array, and places all smaller to left
// of pivot and all greater elements to right of pivot
static int partition(int[] arr, int low, int high)
{
	// Choosing the pivot
	int pivot = arr[high];

	// Index of smaller element and indicates
	// the right position of pivot found so far
	int i = low - 1;

	for (int j = low; j <= high - 1; j++) {

		// If current element is smaller than the pivot
		if (arr[j] < pivot) {

			// Increment index of smaller element
			i++;
			int temp = arr[i];
			arr[i] = arr[j];
			arr[j] = temp;
		}
	}
	
	i++;
	int temp = arr[i];
	arr[i] = arr[high];
	arr[high] = temp;

	return i;
}
```

<br>

# 
---
- [QuickSort - GeeksforGeeks](https://www.geeksforgeeks.org/quick-sort/)