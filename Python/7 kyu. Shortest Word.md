# Shortest Word

Simple, given a string of words, return the length of the shortest word(s).

String will never be empty and you do not need to account for different data types.

# Solution
```
def find_short(s):
    l = min([len(i) for i in s.split()])   
    return l # l: shortest word length
```