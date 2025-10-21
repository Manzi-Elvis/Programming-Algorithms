#  Selection Sort Algorithm

##  Description
Selection Sort is a simple comparison-based sorting algorithm.  
It works by repeatedly selecting the **smallest (or largest)** element from the **unsorted portion** of the array and swapping it with the **first unsorted element**, effectively growing the sorted part of the list one element at a time.

---

##  How It Works (Step-by-Step)
Let’s sort `[5, 3, 8, 1, 2]` in ascending order:

1. **Find the smallest element** in the entire array → `1`  
   Swap it with the first element → `[1, 3, 8, 5, 2]`
2. **Find the smallest in remaining part `[3, 8, 5, 2]`** → `2`  
   Swap it with the first unsorted element (`3`) → `[1, 2, 8, 5, 3]`
3. **Find the smallest in `[8, 5, 3]`** → `3`  
   Swap it with `8` → `[1, 2, 3, 5, 8]`
4. **Find smallest in `[5, 8]`** → `5` (already in place)
5.  Done — array is sorted!

---

##  Pseudocode
```
 procedure selectionSort(arr)
  n = length(arr)
  for i = 0 to n - 2 do
   minIndex = i
   for j = i + 1 to n - 1 do
    if arr[j] < arr[minIndex] then
    minIndex = j
   swap arr[i] and arr[minIndex]
  end for
 end procedure
```

---

##  Complexity Analysis

| Case    | Time Complexity |
|---------|-----------------|
| Best    | O(n²)           |
| Average | O(n²)           |
| Worst   | O(n²)           |

- **Space Complexity:** O(1)  
- **Stable:**  (not stable)  
- **In-place:** (stable)  

---

##  Code Example (Python)
```python
def selection_sort(arr):
    n = len(arr)
    for i in range(n - 1):
        min_index = i
        for j in range(i + 1, n):
            if arr[j] < arr[min_index]:
                min_index = j
        arr[i], arr[min_index] = arr[min_index], arr[i]
    return arr
```
# Example
```
nums = [5, 3, 8, 1, 2]
print("Sorted:", selection_sort(nums))
```

##  Use Cases
- Good for small datasets or teaching
- Great when memory usage must be minimal
- Avoid for large datasets (slow)

##  Exercises

1. Implement Selection Sort in descending order.
2. Modify it to return both the sorted list and the number of swaps made.
3. Sort a list of strings alphabetically using Selection Sort.
4. Trace the algorithm for `  [9, 1, 4, 3, 7] ` — show steps.
5. Compare the number of swaps between Selection Sort and Bubble Sort for ` [4, 3, 2, 1] `