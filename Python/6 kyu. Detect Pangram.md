# Detect Pangram

A pangram is a sentence that contains every single letter of the alphabet at least once. For example, the sentence "The quick brown fox jumps over the lazy dog" is a pangram, because it uses the letters A-Z at least once (case is irrelevant).

Given a string, detect whether or not it is a pangram. Return True if it is, False if not. Ignore numbers and punctuation.

# Solution
```
def is_pangram(s):
    from string import ascii_uppercase
    count = len(ascii_uppercase)
    l = []
    for i in s.upper():
        if i in ascii_uppercase and i not in l:
            l.append(i)
    return len(l) == count            
```