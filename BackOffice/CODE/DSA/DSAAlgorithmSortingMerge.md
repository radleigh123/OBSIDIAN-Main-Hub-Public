---
cssclasses:
- hide-header-underline-2
aliases: []
tags:
- DSA/Algorithm/Sorting 
---
**[[DSAAlgorithmSorting|BACK]]**

---
## Merge Sort
works by dividing an array into smaller subarrays, sorting each subarray, and then merging the sorted subarrays back together to form the final sorted array.

>[!aside|right]-
> ```
> 5 6 7 11 12 13 
> ```

```java
int arr[] = { 12, 11, 13, 5, 6, 7 };

// Merges two subarrays of arr[].
// First subarray is arr[l..m]
// Second subarray is arr[m+1..r]
void merge(int arr[], int l, int m, int r)
{
	// Find sizes of two subarrays to be merged
	int n1 = m - l + 1;
	int n2 = r - m;

	// Create temp arrays
	int L[] = new int[n1];
	int R[] = new int[n2];

	// Copy data to temp arrays
	for (int i = 0; i < n1; ++i)
		L[i] = arr[l + i];
	for (int j = 0; j < n2; ++j)
		R[j] = arr[m + 1 + j];

	// Merge the temp arrays

	// Initial indices of first and second subarrays
	int i = 0, j = 0;

	// Initial index of merged subarray array
	int k = l;
	while (i < n1 && j < n2) {
		if (L[i] <= R[j]) {
			arr[k] = L[i];
			i++;
		}
		else {
			arr[k] = R[j];
			j++;
		}
		k++;
	}

	// Copy remaining elements of L[] if any
	while (i < n1) {
		arr[k] = L[i];
		i++;
		k++;
	}

	// Copy remaining elements of R[] if any
	while (j < n2) {
		arr[k] = R[j];
		j++;
		k++;
	}
}

// Main function that sorts arr[l..r] using
// merge()
void sort(int arr[], int l, int r)
{
	if (l < r) {

		// Find the middle point
		int m = l + (r - l) / 2;

		// Sort first and second halves
		sort(arr, l, m);
		sort(arr, m + 1, r);

		// Merge the sorted halves
		merge(arr, l, m, r);
	}
}
```

**Alternative**
```java
static void mergeSort(int[] arr)
{
	int n = arr.length;

	if (n <= 1) {
		return;
	}

	int mid = n / 2;
	int[] leftArr = new int[mid];
	int[] rightArr = new int[n - mid];

	int i = 0;
	int j = 0;

	for (; i < n; i++) {
		if (i < mid) {
			leftArr[i] = arr[i];
		} else {
			rightArr[j] = arr[i];
			j++;
		}
	}

	mergeSort(leftArr);
	mergeSort(rightArr);
	merge(leftArr, rightArr, arr);
}

static void merge(int[] leftArr, int[] rightArr, int[] arr)
{
	int leftSize = arr.length / 2;
	int rightSize = arr.length - leftSize;
	// indices
	int i = 0;
	int l = 0;
	int r = 0;

	while (l < leftSize && r < rightSize) {
		if (leftArr[l] < rightArr[r]) {
			arr[i] = leftArr[l];
			i++;
			l++;
		} else {
			arr[i] = rightArr[r];
			i++;
			r++;
		}
	}

	while (l < leftSize) {
		arr[i] = leftArr[l];
		i++;
		l++;
	}

	while (r < rightSize) {
		arr[i] = rightArr[r];
		i++;
		r++;
	}
}
```

<br>

# 
---
- [Merge Sort - GeeksforGeeks](https://www.geeksforgeeks.org/merge-sort/)