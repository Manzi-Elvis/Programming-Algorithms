# 🫧 Bubble Sort Algorithm

##  Description  
The **Bubble Sort** algorithm is like teaching numbers how to “float” into their correct positions — one tiny swap at a time.  

It repeatedly steps through the list, compares adjacent pairs, and swaps them if they’re in the wrong order.  
This process continues until no swaps are needed, meaning everything is finally in order.  

Imagine a line of people arranged by height — Bubble Sort is the friend who keeps swapping anyone who’s taller than the person next to them until the entire group looks perfect 👌.

---

##  Algorithm Type  
This is a **Comparison-Based Sorting Algorithm** — specifically a **Simple Iterative Algorithm**.  
It uses pairwise comparisons and repeated passes to sort a collection.  

It’s one of the easiest sorting algorithms to understand (and to code), which is why it’s often taught first — even though it’s not the fastest for large data sets.

---

##  Use Cases  
Even though it’s not efficient for big data, Bubble Sort still shines in:
-  **Learning purposes** — great for beginners to understand how sorting works step by step.  
-  **Nearly sorted data** — performs fairly well when the list is almost sorted.  
-  **Educational visualizations** — often used in algorithm animations to demonstrate sorting principles.

---

##  Approach  
1. Start at the beginning of the array.  
2. Compare each pair of adjacent elements.  
3. If the first element is greater than the second, **swap them**.  
4. Continue through the array — after the first pass, the largest element will have “bubbled up” to the end.  
5. Repeat the process, ignoring the last sorted elements each time, until the list is completely sorted.  

---

##  Time & Space Complexity  
| Case | Time Complexity | Space Complexity |
|------|-----------------|------------------|
| **Best Case (already sorted)** | O(n) | O(1) |
| **Average Case** | O(n²) | O(1) |
| **Worst Case (reverse order)** | O(n²) | O(1) |

  *Bubble Sort is an in-place algorithm (it doesn’t need extra space), but it’s not ideal for large data sets due to its quadratic time complexity.*

---

##  Pseudocode  
```plaintext
FUNCTION bubbleSort(array)
    n ← length of array
    FOR i FROM 0 TO n - 1 DO
        swapped ← false
        FOR j FROM 0 TO n - i - 2 DO
            IF array[j] > array[j + 1] THEN
                SWAP array[j] WITH array[j + 1]
                swapped ← true
            END IF
        END FOR
        IF NOT swapped THEN
            BREAK
        END IF
    END FOR
    RETURN array
END FUNCTION
