# Anagram Checker  

## Description  
If two words use **exactly the same letters** but in a different order — you’ve got an *anagram*.  
It’s like “recycling” letters to make new words.  

For example:  
- `listen` → `silent`  
- `evil` → `vile`  
- `angel` → `glean`  

In essence, both words contain the same ingredients, just mixed differently.  
Anagram checkers are all about verifying that two strings are made of the same characters with the same frequency.

---

## Use Cases  
- **Word games & puzzles:** Scrabble, crosswords, and word jumble solvers love this.  
- **Plagiarism & text similarity detection:** Can help detect rearranged but identical content.  
- **Data validation:** Ensures consistency when string elements are supposed to match in composition.  
- **Interview questions:** This one’s a favorite — simple logic, big insight.

---

## Complexity  
- **Time Complexity:** O(n), assuming you’re using hashing or sorting (where *n* is the length of the words).  
- **Space Complexity:** O(1) if using fixed-size character counting, or O(n) if using maps/dictionaries.  

---

## Approach  
There are two common ways to check if two strings are anagrams:  

### 1. **Sorting Approach**  
Sort both strings alphabetically and compare them.  
If both sorted versions are identical, they’re anagrams.  

### 2. **Counting Approach**  
Count how many times each letter appears in both strings.  
If both counts match perfectly, it’s an anagram.  

The counting method is usually faster since you don’t actually sort anything.  

---

## Example Thought  
Think of both words as bags of letter tiles.  
If every tile in bag A has a matching twin in bag B — same letter, same quantity — you’ve got an anagram.  
If one bag has an extra “t” or missing “e,” it’s game over.  

---

## Pseudocode  

if length(str1) != length(str2):
    return false

countMap = empty map

for char in str1:

    countMap[char] = countMap.get(char, 0) + 1

for char in str2:

    if char not in countMap:
    
        return false

    countMap[char] -= 1

    if countMap[char] < 0:
    
        return false

return true


---

## Try It Yourself  
- Write the sorting-based version and compare its performance to the counting version.  
- Update your checker so it ignores spaces and punctuation:  
  `"Dormitory"` and `"Dirty room!"` should return `True`.  
- Modify it to handle full sentences.  
- Extend it to detect **multi-word anagrams**, like:  
  `"The eyes"` ↔ `"They see"`.  

---

##  Exercises  

**1. Basic Check**  
Implement a simple anagram function using the sorting method.  

**2. Case & Space Insensitivity**  
Make your function ignore casing and whitespace.  
Example: `"Debit Card"` and `"Bad Credit"` → `True`  

**3. Word List Filter**  
Given a list of words, return all anagrams of a given word.  
Example:  
Input: `["enlist", "google", "inlets", "banana"]`, Word: `"listen"`  
Output: `["enlist", "inlets"]`

**4. Group Anagrams**  
Given a list of words, group them by anagrams.  
Example:  
`["bat", "tab", "tap", "pat", "cat"]` → `[["bat", "tab"], ["tap", "pat"], ["cat"]]`  

**5. Character Frequency Visualizer (Challenge)**  
Write a small function that prints the frequency of each letter in both strings side by side,  
to help visualize why two words are or aren’t anagrams.  

---

 *Tip:* This algorithm is a small but powerful way to practice thinking in terms of *patterns, frequency, and structure* — the same ideas behind hash maps, machine learning feature extraction, and more.
