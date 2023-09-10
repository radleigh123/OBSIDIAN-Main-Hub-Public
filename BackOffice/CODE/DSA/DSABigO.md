---
cssclass:
aliases:
tags:
---
**[[DSA|HOME [DSA]]]**

---
## Big-O Notation
> The **O** comes from the "**O**rder of magnitude of complexity".

represents the <mark class="hltr-lightblue">**upper bound** of the running time of an algorithm</mark>. Thus, it gives the worst-case complexity of an algorithm.

Since it gives the worst-case running time of an algorithm, it is widely used to analyze an algorithm as we are always interested in the worst-case scenario.
>[!caption|center]
> ![[DSABigO.png|center hs-med]]
> Big-O gives the upper bound of a function

>[!NOTE|clean no-i collapse]- Explanation
> ```
> O(g(n)) = {
> 	f(n): there exist positive constants c and n0
> 	such that 0 ≤ f(n) ≤ cg(n) for all n ≥ n0
> }
> ```
> The above expression can be described as a function `f(n)` belongs to the set `O(g(n))` if there exists a positive > constant `c` such that it lies between `0` and `cg(n)`, for sufficiently large `n`.
> 
> For any value of `n`, the running time of an algorithm does not cross the time provided by `O(g(n))`.

<br>

### Major complexities
- **O(1)**: <mark class="hltr-lightgreen">constant time</mark>,
	- every time a constant amount of time is required to execute code, no matter which operating system or which machine configurations you are using.
	- when your calculation is not dependent on the input size
	```java
	System.out.println("Hello World");
	```
- **O(log n)**: <mark class="hltr-lightgreen">logarithmic time</mark>,
	- divide into two, repeat the process till left with one value
	- when the input size is reduced by half, maybe when iterating, handling recursion, or whatsoever
	```java
	// similar to LINEAR TIME, except half of the input size
	int target = 55;
	
	int start = 0;
	int end = array.length - 1;
	
	while(start <= end) {
		int middle = (start + end) / 2;

		if (array[middle] == target) {
			return middle;
		}

		if (array[middle] > target) {
			end = middle - 1;
		} else {
			start = middle + 1;
		}
	}
	
	return -1
	```
- **O(n)**: <mark class="hltr-lightgreen">linear time</mark>,
	- every time, a linear amount of time is required to execute code.
	- when you have a single loop within your algorithm
	```java
	// runtime depends on the input size
	for (int i = 0; i < input; i++) {
		System.out.println("Hello World");
	}
	```
- **O(n log n)**: <mark class="hltr-lightgreen">quasilinear runtime</mark>,
	- used with [[DSAAlgorithmSortingMerge|Merge Sort]]
- **O(n²)**: <mark class="hltr-lightgreen">quadratic time</mark>,
	- similar with multidimensional loops
	- when you have nested loops within your algorithm, meaning a loop in a loop
	```java
	// horrible time complexity
	for (int i = 0; i < input; i++) {
		for (int j = 0; j < input; j++) {
			System.out.println("Hello World");
		}
	}
	```

>[!FAIL] Inefficient runtime
>- **O(2*n)**: exponential time
>	- when the growth rate doubles with each addition to the input
> 	```java
> 	public int recursiveMethod(int n) {
> 		if (n < 2) {
> 			return n;
> 		}
> 		
> 		return recursiveMethod(n - 1) + recursiveMethod(n - 2);
> 	}
> 	```
>- **O(nm)**: brute force runtime
>	- if we were to search for a string of `n` characters in a string of `m` characters, it would take us `n * m` tries.
>- **O(n!)**: factorial time/traveling salesman runtime

<br>

# 
---
- [Big-O Notation (Asymptotic Analysis)](https://www.programiz.com/dsa/asymptotic-notations#google_vignette)
- [Big O Cheat Sheet ](https://www.freecodecamp.org/news/big-o-cheat-sheet-time-complexity-chart/)