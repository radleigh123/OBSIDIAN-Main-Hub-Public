---
cssclasses:
- t-w
- table-nalt
- table-b
- table
aliases: []
tags:
- DSA/Algorithm/Sorting
---
**[[DSAAlgorithm|BACK]]**

---
## Sorting Algorithm
is used to rearrange a given array or list of elements according to a comparison operator on the elements. The comparison operator is used to decide the new order of elements in the respective data structure.
>[!column|flex no-t collapse]
>>[!NOTE|clean no-t]
>>- [[DSAAlgorithmSortingSelection|Selection Sort]]
>>- [[DSAAlgorithmSortingBubble|Bubble Sort]]
>>- [[DSAAlgorithmSortingInsertion|Insertion Sort]]
>>- [[DSAAlgorithmSortingMerge|Merge Sort]]
>>- [[DSAAlgorithmSortingQuickSort|QuickSort]]
>>- Heap Sort
>>- Counting Sort
>>- Radix Sort
>>- Bucket Sort
>>- Bingo Sort Algorithm
>>- [[DSAAlgorithmSortingShellSort|ShellSort]]
>>- TimSort
>>- Comb Sort
>>- Pigeonhole Sort
>
>>[!NOTE|clean no-t]
>>- Cycle Sort
>>- Cocktail Sort
>>- Strand Sort
>>- Bitonic Sort
>>- Pancake sorting
>>- BogoSort or Permutation Sort
>>- Gnome Sort
>>- Sleep Sort – The King of Laziness
>>- Structure Sorting in C++
>>- Stooge Sort
>>- Tag Sort (To get both sorted and original)
>>- Tree Sort
>>- Odd-Even Sort / Brick Sort
>>- 3-way Merge Sort

<br>

**Table of Complexity Comparison:**

| Name                                      | Best Case   | Worst Case  | Memory      | Stable                                   | Method Used         |
| ----------------------------------------- | ----------- | ----------- | ----------- | ---------------------------------------- | ------------------- |
| **<center>QuickSort</center>**            | $n\ log\ n$ | $n^2$       | $log\ n$    | No                                       | Partitioning        |
| **<center>Merge Sort</center>**           | $n\ log\ n$ | $n\ log\ n$ | $n\ log\ n$ | <mark class="hltr-lightgreen">Yes</mark> | Merging             |
| **<center>Heap Sort</center>**            | $n\ log\ n$ | $n\ log\ n$ | $1$         | No                                       | Selection           |
| **<center>Insertion Sort</center>**       | $n$         | $n^2$       | $1$         | <mark class="hltr-lightgreen">Yes</mark> | Insertion           |
| **<center>Tim Sort</center>**             | $n$         | $n\ log\ n$ | $n$         | <mark class="hltr-lightgreen">Yes</mark> | Insertion & Merging |
| **<center>Selection Sort</center>**       | $n^2$       | $n^2$       | $1$         | No                                       | Selection           |
| **<center>ShellSort</center>**            | $n\ log\ n$ | $n^{3/2}$   | $1$         | No                                       | Insertion           |
| **<center>Bubble Sort</center>**          | $n$         | $n^2$       | $1$         | <mark class="hltr-lightgreen">Yes</mark> | Exchanging          |
| **<center>Tree Sort</center>**            | $n\ log\ n$ | $n\ log\ n$ | $n$         | <mark class="hltr-lightgreen">Yes</mark> | Insertion           |
| **<center>Cycle Sort</center>**           | $n^2$       | $n^2$       | $1$         | No                                       | Selection           |
| **<center>Strand Sort</center>**          | $n$         | $n^2$       | $n$         | <mark class="hltr-lightgreen">Yes</mark> | Selection           |
| **<center>Cocktail Shaker Sort</center>** | $n$         | $n^2$       | $1$         | <mark class="hltr-lightgreen">Yes</mark> | Exchanging          |
| **<center>Comb Sort</center>**            | $n\ log\ n$ | $n^2$       | $1$         | No                                       | Exchanging          |
| **<center>Gnome Sort</center>**           | $n$         | $n^2$       | $1$         | <mark class="hltr-lightgreen">Yes</mark> | Exchanging          |
| **<center>Odd-even Sort</center>**        | $n$         | $n^2$       | $1$         | <mark class="hltr-lightgreen">Yes</mark> | Exchanging          |


<br>

# 
---
- [Sorting Algorithms - GeeksforGeeks](https://www.geeksforgeeks.org/sorting-algorithms/?ref=lbp)