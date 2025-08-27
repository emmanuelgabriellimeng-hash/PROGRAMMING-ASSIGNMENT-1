# PA 1 – Introduction to Python Programming

## Overview

This experiment explores the foundational elements of Python programming such as string manipulation, list handling, function creation, dictionary use, and user input processing.
## Directory
Alphabet Soup Problem: https://github.com/emmanuelgabriellimeng-hash/PROGRAMMING-ASSIGNMENT-1/blob/main/README.md#alphabet-soup-problem

Emoticon Problem: https://github.com/emmanuelgabriellimeng-hash/PROGRAMMING-ASSIGNMENT-1/blob/main/README.md#emoticon-problem

Unpacking Problem: https://github.com/emmanuelgabriellimeng-hash/PROGRAMMING-ASSIGNMENT-1/blob/main/README.md#unpacking-list-problem

## Program Link
### https://github.com/emmanuelgabriellimeng-hash/PROGRAMMING-ASSIGNMENT-1/blob/main/LIM_2ECEB_Experiment_1.ipynb

## Alphabet Soup Problem

**Description:**  
Write a function that takes a string as input and outputs the same string with its characters sorted in alphabetical (lexicographical) order.

---
**Explanation**  

1. Define the function `alphabet_soup` with variable `t` as the input text.
```python
def alphabet_soup(t):
```

2. Applying `sorted()` function to sort characters in `t`, then include `''.join()` to concatenate. Afterwards, enclose these commands inside `print()`.
```python
        print(''.join(sorted(t)))
```

3. Finally, call the function on user input.
```python
alphabet_soup(input("Sort any text:"))
```
**Example**
```python
print(emotify("Sir tapos na po :D"))
```

**Expected Output**
```python
    ,:DSaainoopprst
```
---
## Emoticon Problem

**Description**  
Create a function that changes specific words into emoticons. Given a sentence as a string, replace the words smile, grin, sad, and mad with their corresponding emoticon:
| Word  | Emoticon |
|-------|----------|
| smile | :)       |
| grin  | :D       |
| sad   | :(       |
| mad   | >:(      |


---
**Explanation**  

1. Import the `string` module to access `string.punctuation`.
```python
import string
```

2. Define the function `emotify` with variable `t` as the input text.
```python
def emotify(t):
```

3. Declare `emojis` as a dictionary structure with lowercase keywords and their corresponding emoticons.
```python
    emojis = {"sad": ":(", "grin": ":D", "mad": ">:(", "smile": ":)"}
```

4. Initialize list `sentence` to store processed words.
```python
    sentence = []
```

5. Apply `for` loop with function `t.split` to separate text into words per iteration.
```python
    for word in t.split():
```

6. Remove attached punctuation from the word using `strip(string.punctuation)` and store within `emojiKey`.
```python
        emojiKey = word.strip(string.punctuation)
```

7. Using `emojis.get()`, the lowercase version of `emojiKey` locates the emoticons in `emojis` dictionary, and if it does not exist, the original `emojiKey` is kept as default.
```python
        emoji = emojis.get(emojiKey.lower(), emojiKey)
```

8. Replace the first occurrence of `emojiKey` inside the `word` list with the `emoji` to maintain the punctuation.
```python
        emotified_word = word.replace(emojiKey, emoji, 1)
```

9. Using `sentence.append()`, the processed `emotified_word` is added into the `sentence` list.
```python
        sentence.append(emotified_word)
```

10. Combine all items from the `sentence` list into one string separated by spaces and return it as the final result.
```python
    return " ".join(sentence)
```

**Example**

```python
print(emotify("Sir, tapos na po SmILe gRIN sad MAd."))
```

**Expected Output**

```python
Sir, tapos na po :) :D :( >:(.
```

## Unpacking List Problem

**Description:**  
Unpack the list writeyourcodehere into three variables, being first, middle, and last, with middle being everything in between the first and last element. Then print all three variables.

---

**Explanation**

1. Convert the string `"writeyourcodehere"` into a list of characters, then store it inside `t_list`.
```python
t_list = list("writeyourcodehere")
```

2. Remove the first character from `t_list` using `pop(0)` and assign it to `first`.

```python
first = t_list.pop(0)
```

3. Remove the last character from `t_list` using `pop(-1)` and assign it to `last`.
```python
last = t_list.pop(-1)
```

4. Assign the remaining characters to `middle`.
```python
middle = t_list
```

5. Print the value stored in `first`, `middle`, and `last`.
```python
print("first:", first)
print("middle:", middle)
print("last:", last)
```
**Expected Output**
```python
first: w
middle: ['r', 'i', 't', 'e', 'y', 'o', 'u', 'r', 'c', 'o', 'd', 'e', 'h', 'e', 'r']
last: e
```
