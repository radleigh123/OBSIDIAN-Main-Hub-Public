---
cssclasses:
- hide-header-underline-2
aliases: []
tags:
- DSA/Algorithm/Sorting 
---
**[[DSAAlgorithmSorting|BACK]]**

---
## Bubble Sort
is the <mark class="hltr-lightgreen">simplest sorting algorithm</mark> that works by repeatedly swapping the adjacent elements if they are in the wrong order. This algorithm is <mark class="hltr-lightred">not suitable for large data sets</mark> as its average and worst-case time complexity is quite high.
```java
int n = arr.length;
int i, j, temp;
boolean swapped;

for (i = 0; i < n - 1; i++) {
	swapped = false;
	
	for (j = 0; j < n - i - 1; j++) {
		if (arr[j] > arr[j + 1]) { 
			// Swap arr[j] and arr[j+1]
			temp = arr[j];
			arr[j] = arr[j + 1];
			arr[j + 1] = temp;
			swapped = true;
		}
	}

	// If no two elements were
	// swapped by inner loop, then break
	if (swapped == false) {
		break;
	}
}
```

**Examples**
- [[DSASortingExample|Bubble sort example]]

<br>

# 
---
- [Bubble Sort - Data Structure and Algorithm Tutorials - GeeksforGeeks](https://www.geeksforgeeks.org/bubble-sort/?ref=outind)