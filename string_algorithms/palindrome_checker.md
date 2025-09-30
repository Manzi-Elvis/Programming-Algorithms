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
while left < right:
    if str[left] != str[right]:
        return false
    left++
    right--

return true
