# Experiment 1 – Introduction to Python Programming

## Overview

This experiment explores the foundational elements of Python programming through hands-on problem-solving. The notebook introduces key concepts such as string manipulation, list handling, function creation, dictionary use, and user input processing. The tasks are designed to build core programming competencies applicable to engineering and computing disciplines.

## Objective

- To develop familiarity with basic Python syntax and logic structures.
- To apply standard Python operations for string and list processing.
- To practice writing functions that accept user input and return structured output.
- To reinforce understanding of code readability and modular programming.

## Tools and Environment

- **Language:** Python 3.13.5  
- **Development Environment:** Jupyter Notebook (or compatible IDE)  
- **Libraries Used:** Built-in Python standard libraries (`string`)  
- **Platform Compatibility:** Cross-platform (Windows, macOS, Linux)

## Problem 1 – Alphabetical Sorting of Characters

**Problem Statement:**  
Write a function that takes a string as input and outputs the same string with its characters sorted in alphabetical (lexicographical) order.

---

**Step-by-Step Explanation:**  

1. **Input:**  
   The function accepts a string. For example:  
   `"Sir, tapos na po :D"`

2. **Sorting Characters:**  
   - Python's built-in function `sorted()` can be applied to a string.  
   - `sorted()` treats the string as a sequence of characters and returns a list of those characters sorted according to their Unicode (ASCII) values.  
   - The sorting order is case-sensitive:  
     - All uppercase letters (A-Z) come before lowercase letters (a-z).  
     - Spaces, punctuation, and special characters are also sorted based on their Unicode values.

3. **Reconstructing the String:**  
   - The output of `sorted()` is a list of characters.  
   - We use the `join()` method to combine these characters back into a single string.

4. **Output:**  
   - The function prints the sorted string.  
   - For the example input, the output would be:  
     `"    ,:DSaainoopprst"`  
   - Notice that spaces and punctuation are included and sorted along with the letters.
---
## Problem 2 – Emoticon Replacement

**Problem Statement:**  
Create a function that takes a sentence as input and replaces specific emotion words with their corresponding emoticons:

| Word  | Emoticon |
|-------|----------|
| smile | :)       |
| grin  | :D       |
| sad   | :(       |
| mad   | >:(      |

The replacement should be case-insensitive and punctuation must be preserved.

---

### Process Description

1. **Receive input sentence:**  
   The function accepts a sentence as a string, e.g., `"Make me smile!"`.

2. **Define emoticon dictionary:**  
   A dictionary maps keywords to emoticons, enabling fast lookup:  
   ```python
   {
       "sad": ":(",
       "grin": ":D",
       "mad": ">:(",
       "smile": ":)"
   }
3. **Split sentence into words:**  
   The input sentence is split into individual words using whitespace as the delimiter.  
   This allows the function to process each word independently.

4. **Strip punctuation from each word:**  
   Each word may have punctuation marks attached at the beginning or end (such as commas, periods, exclamation points).  
   Using the `string.punctuation` constant, these marks are stripped away to isolate the core word for matching.

5. **Convert the core word to lowercase:**  
   To make matching case-insensitive, the core word is converted to lowercase.  
   For example, "SmIlE" and "smile" will both match the dictionary key `"smile"`.

6. **Lookup the emoticon:**  
   The lowercase core word is checked against the emoticon dictionary keys.  
   - If a match is found, retrieve the corresponding emoticon.  
   - If no match, keep the original core word unchanged.

7. **Replace the core word with the emoticon in the original word:**  
   The original word may contain punctuation.  
   To preserve it, replace only the core word inside the original word with the emoticon, leaving punctuation intact.

8. **Reconstruct the sentence:**  
   All processed words are combined back into a single string, maintaining spaces between them, to produce the final emotified sentence.

---
## Problem 3 – List Unpacking

**Problem Statement:**  
Given the string `"writeyourcodehere"`, unpack its characters into three variables:

- `first`: the first character  
- `middle`: a list containing all characters between the first and last characters  
- `last`: the last character

Print the values of all three variables.

---

### Process Description

1. **Convert the string to a list:**  
   Since strings are immutable in Python (cannot be changed), convert the string into a list of characters.  
   This allows easy removal and manipulation of elements.

2. **Extract the first character:**  
   Use the `pop(0)` method to remove and store the first character of the list.

3. **Extract the last character:**  
   Use the `pop(-1)` method to remove and store the last character of the list.

4. **Assign the remaining characters to `middle`:**  
   After removing the first and last characters, the remaining elements of the list constitute the middle section.

5. **Print the results:**  
   Display the values of `first`, `middle`, and `last` to verify that unpacking was successful.
