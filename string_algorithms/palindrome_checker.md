# Palindrome Checker  

## Description  
A palindrome is like that friend who looks the same in every photo, no matter which way you flip the picture.  
It’s a word, phrase, or number that reads the same backward and forward.  

Examples?  
- `madam`  
- `racecar`  
- `1221`  

The concept is simple, but it’s one of those classic coding exercises that sneaks its way into interviews, puzzles, and practice problems.  

---

## Use Cases  
- **Coding interviews:** This problem is almost a rite of passage.  
- **Word/number puzzles:** Think of games or challenges that need pattern checking.  
- **Text processing:** Spell checkers, filters, and validators often rely on checks like this.  
- **Bioinformatics:** Palindromic DNA sequences actually exist, and this logic helps detect them.  

---

## Complexity  
- **Time Complexity:** O(n), since you might compare every character.  
- **Space Complexity:** O(1) if you check characters in place, or O(n) if you reverse a copy.  

---

## Approach  
Here’s the neat trick:  

1. **Clean the input.** Lowercase it and strip out weird stuff like punctuation (`"Madam!"` should still pass).  
2. **Mirror comparison.** Start at both ends and compare characters moving inward.  
3. If all pairs match, it’s a palindrome. If one doesn’t, game over.  

Think of it like closing a zipper — each tooth (character) has to match perfectly as you zip inward.  

---

## Pseudocode
```  
while left < right:
    if str[left] != str[right]:
        return false
    left++
    right--

return true
```

##  Exercises

Let’s see how well you understood the logic behind palindromes.  
Try these challenges — don’t rush, and remember: the goal isn’t to finish fast, it’s to understand *why* your solution works.

---

**1. The Basic Check**  
Write a function that checks if a given string is a palindrome *without* using any built-in reverse functions (like `[::-1]` in Python).  
*Hint:* Use two pointers, one at the start and one at the end.

---

**2. Ignore the Noise**  
Update your palindrome checker so it ignores punctuation, spaces, and letter casing.  
Example:  
`"A man, a plan, a canal: Panama"` → should return `True`

---

**3. Number Palindrome**  
Modify your function to handle numbers too.  
Example:  
`12321` → `True`  
`120021` → `False`

---

**4. Find All Palindromes in a List**  
Given a list of words, return only the palindromes.  
Example:  
`["racecar", "python", "madam", "hello", "level"]` → `["racecar", "madam", "level"]`

---

**5. Longest Palindromic Substring (Challenge Mode 🧠)**  
Given a string, find the longest substring that is a palindrome.  
Example:  
`"babad"` → `"bab"` or `"aba"`  
This one’s a classic interview question — if you nail it, you’re definitely leveling up.

---

 *Tip:* Once you’re done, try timing your solutions on long strings. Performance matters more than you think.