---
cssclass:
aliases:
tags:
---
**[[DSA|HOME [DSA]]]**

---
>[!aside|right]-
> ```
> Linear Search took: 39 milliseconds
> Binary Search took: 0 milliseconds
> Recursive Binary Search took: 0 milliseconds
> ```

```java
class Solution {
    public static void main(String[] args) {
        int[] list = new int[100_000_000];

        for (int i = 0; i < list.length; i++) {
            list[i] = i + 1;
        }

        long start = System.currentTimeMillis();
        linearSearch(list, list.length);
        print("Linear Search", start);

        start = System.currentTimeMillis();
        binarySearch(list, list.length);
        print("Binary Search", start);

        start = System.currentTimeMillis();
        recursiveBinarySearch(list, 0, list.length - 1, list.length);
        print("Recursive Binary Search", start);
    }

    public static int linearSearch(int[] list, int target) {
        // O(n)
        for (int i = 0; i < list.length; i++) {
            if (list[i] == target) {
                return i;
            }
        }
        return -1;
    }

    public static int binarySearch(int[] list, int target) {
        // O(log n)
        int start = 0;
        int end = list.length - 1;
        while (start <= end) {
            int middle = (start + end) / 2;

            if (list[middle] == target) {
                return middle;
            }

            if (list[middle] > target) {
                end = middle - 1;
            } else {
                start = middle + 1;
            }
        }

        return -1;
    }

    public static int recursiveBinarySearch(int[] list, int start, int end, int target) {
        if (list.length == 0) {
            return -1;
        }

        if (!(start <= end)) {
            return -1;
        }

        int middle = (start + end) / 2;

        if (list[middle] == target) {
             return middle;
        } else if (list[middle] < target) {
            start = middle + 1;
            return recursiveBinarySearch(list, start, end, target);
        } else {
            end = middle - 1;
            return recursiveBinarySearch(list, start, end, target);
        }

        /* // Alternative, given by ChatGPT
        if (start <= end) {
            int middle = start + (end - start) / 2;

            if (list[middle] == target) {
                return middle;
            } else if (list[middle] < target) {
                return recursiveBinarySearch(list, middle + 1, end, target);
            } else {
                return recursiveBinarySearch(list, start, middle - 1, target);
            }
        }

        return -1; // element not found */
    }

    public static void print(String string, long start) {
        System.out.println(string + " took: " + (System.currentTimeMillis() - start) + " milliseconds");
    }
}
```