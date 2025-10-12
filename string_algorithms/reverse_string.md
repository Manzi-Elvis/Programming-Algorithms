# Reverse String  

## Description  
Reversing a string might sound too basic, but it’s one of those small ideas that build the foundation for bigger ones — recursion, data structures, even cryptography tricks.  

The goal is simple:  
Take `"hello"` → return `"olleh"`.  

But what’s cool is **how many ways** you can actually reverse a string — loops, stacks, recursion, slicing, you name it.  
This one teaches you to think about strings as sequences you can manipulate, not just text to print.

---

## Use Cases  
- **String manipulation:** Useful in building text editors, formatters, or parsers.  
- **Algorithm warm-ups:** Common first problem to learn iteration or recursion.  
- **Data encoding/decoding:** Sometimes reversing is part of simple cipher operations.  
- **Interview practice:** A classic “can you think step-by-step?” type of question.

---

## Complexity  
- **Time Complexity:** O(n) — you must visit each character once.  
- **Space Complexity:** O(1) if done in place (for mutable types like arrays), or O(n) for new string creation.  

---

## Approach  

There are several fun ways to reverse a string:  

### 1. **Iterative Approach**  
Start from the end and build your new string character by character.  

### 2. **Two-Pointer Swap**  
Convert the string into a character array.  
Use one pointer at the start, one at the end, and swap them while moving toward the center.  

### 3. **Recursive Approach**  
Base case: if the string has 0 or 1 character, return it.  
Otherwise, reverse everything except the first character — then append that first character to the end.  

Each method teaches you something different about how data flows in a program.  

---

## Pseudocode 
``` 
  function reverseString(str):
   reversed = ""
   for i from length(str) - 1 down to 0:
    reversed = reversed + str[i]
  return reversed
```

**Or, using recursion:**
```
  function reverseString(str):
   if length(str) <= 1:
     return str
  return reverseString(str[1:]) + str[0]
```
---

## Try It Yourself  
- Implement the iterative, recursive, and slicing methods — compare how fast each one runs.  
- Make a version that reverses **each word in a sentence** but keeps the word order the same.  
  Example: `"Elvis codes fast"` → `"sivlE sedoc tsaf"`.  
- Try reversing a string *in place* using an array of characters.  
- Reverse strings with Unicode or emojis and see what breaks — that’s where encoding knowledge comes in handy.  

---

##  Exercises  

**1. Basic Reverse**  
Write a simple function that reverses `"hello"` into `"olleh"`.  

**2. Sentence Reverse**  
Reverse entire sentences while preserving spaces and punctuation.  

**3. Word-by-Word Reverse**  
Reverse each individual word but not their order.  
Input: `"I love programming"` → Output: `"I evol gnimmargorp"`  

**4. Recursive Reverse**  
Implement a recursive version of the reverse function.  
How does the call stack behave? Print it out to see!  

**5. Palindrome Test (Mini Challenge)**  
Use your reverse function to test if a string is a palindrome.  
Hint: `return s == reverse(s)`

---

*Tip:*  
This simple exercise quietly teaches **control flow**, **looping**, and **memory handling** — things you’ll rely on everywhere from reversing arrays to building real data-processing systems.
