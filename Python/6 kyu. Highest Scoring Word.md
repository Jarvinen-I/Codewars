# Highest Scoring Word

Given an array of integers, find the one that appears an odd number of times.

Given a string of words, you need to find the highest scoring word.

Each letter of a word scores points according to its position in the alphabet: ```a = 1, b = 2, c = 3``` etc.

For example, the score of ```abad``` is ```8``` (1 + 2 + 1 + 4).

You need to return the highest scoring word as a string.

If two words score the same, return the word that appears earliest in the original string.

All letters will be lowercase and all inputs will be valid.

# Solution
```
from string import ascii_lowercase
def high(x):
    score = 0
    highest_scoring_word = ''
    for word in x.split():
        count = sum([ascii_lowercase.index(letter) + 1 for letter in word])
        if count > score:
            score = count
            highest_scoring_word = word
    return highest_scoring_word   
```