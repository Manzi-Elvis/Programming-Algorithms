# Binary Search Algorithm

## Description
Binary Search is what happens when you **stop checking things one by one** and start thinking smart .

Instead of searching like:
> “Is it here? No… here? No… here?”

Binary Search says:
> “Let’s **cut the problem in half** every time.”

That’s why it’s **fast**, **elegant**, and **interview-famous**.

---

## The One Golden Rule ⚠️
🚨 **Binary Search ONLY works on SORTED data** 🚨

No sorting?  
No binary search.  
No exceptions.

---

## Basic Idea (In One Line)
> Repeatedly divide the search space in half until the target is found (or not).

---

## How It Works (Step-by-Step)

Let’s search for **7** in this sorted array:
[1, 3, 5, 7, 9, 11, 13]


### Step 1: Pick the Middle

Middle = 7

Boom! Found it instantly.

---

Now let’s search for **11** instead 👇

### Step 1

Middle = 7

- `11 > 7` → ignore left half ❌

### Step 2

Search in: [9, 11, 13]
Middle = 11

🎉 Found!

---

### Worst Case Example (Not Found)
Searching for **4**:

1. Middle = 7 → go left
2. Middle = 3 → go right
3. Middle = 5 → go left
4. Search space empty → Not found

Binary Search never panics.  
It just keeps cutting

---

## Visual Intuition 
Think of guessing a number between **1 and 100**:

- Guess 50 → too high?
- Guess 25 → too low?
- Guess 37 → closer?

That’s Binary Search in real life.

---

## Iterative Approach (Recommended)

### Pseudocode
```


