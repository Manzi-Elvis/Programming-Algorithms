# Factorial Calculator

## Description  
The **Factorial Calculator** is one of the most iconic algorithms in programming — a true rite of passage for every developer.  

It calculates the product of all positive integers up to a given number `n`.  
In math form, it’s written as:  
```n! = n × (n - 1) × (n - 2) × ... × 1```

For example:  
`5! = 5 × 4 × 3 × 2 × 1 = 120`

It’s simple, elegant, and surprisingly useful. Factorials appear in **combinatorics (like counting permutations)**, **probability theory**, and **mathematical modeling**.  

---

##  Use Cases  
Here’s where factorials sneak into real life and code:
-  **Combinatorics**: Calculating combinations or permutations (e.g., how many ways can you arrange books on a shelf?).  
-  **Probability**: Used in computing probabilities in events and outcomes.  
-  **Math & Science**: Factorials show up in statistics, series expansions (like e^x), and physics formulas.  

---

##  Approach  
We can calculate factorials in two main ways:

1. **Recursive Approach** — because factorials naturally define themselves recursively:  
`n! = n × (n - 1)!`
The base case is `0! = 1`.

2. **Iterative Approach** — where we simply loop through the numbers from `1` to `n` and multiply them all.

---

##  Time & Space Complexity  
| Approach  | Time Complexity | Space Complexity         |
|-----------|-----------------|--------------------------|
| Recursive | O(n)            | O(n) (due to call stack) |
| Iterative | O(n)            | O(1)                     |

For most real-world use cases, both perform similarly — but the iterative one avoids stack overflow on large `n`.

---

##  Pseudocode (Recursive)
```
FUNCTION factorial(n)
 IF n == 0 OR n == 1 THEN
     RETURN 1
 END IF
 RETURN n * factorial(n - 1)
END FUNCTION
```
## Pseudocode (Iterative)
```
FUNCTION factorial(n)
    result ← 1
    FOR i FROM 1 TO n DO
        result ← result * i
    END FOR
    RETURN result
END FUNCTION
```
## Example:
### Input:
`n = 5 `
### Process:
`5 × 4 × 3 × 2 × 1 = 120`
### Output:
`120`
---
## Challenge Time:

### Try these mini exercises:

1. Compute 7! manually on paper (trust me, it’s good mental math training).
2. Modify the algorithm to handle large factorials (think 1000!) using Python’s math or decimal libraries.
3. Implement both recursive and iterative versions — then compare which one is faster for n = 1000.
4. Write a factorial program that prints every intermediate multiplication step.
5. Try writing a memoized factorial function to optimize repeated calculations.