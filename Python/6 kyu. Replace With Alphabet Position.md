# Replace With Alphabet Position

Welcome.

In this kata you are required to, given a string, replace every letter with its position in the alphabet.

If anything in the text isn't a letter, ignore it and don't return it.

```"a" = 1```, ```"b" = 2```, etc.

### Example
```
alphabet_position("The sunset sets at twelve o' clock.")
```
Should return ```"20 8 5 19 21 14 19 5 20 19 5 20 19 1 20 20 23 5 12 22 5 15 3 12 15 3 11"``` ( as a string )

# Solution
```
def alphabet_position(text):
    from string import ascii_lowercase
    letters = [i for i in ascii_lowercase]
    numbers = [i for i in range(1, len(letters) + 1)] 
    d = dict(zip(letters, numbers))
    l = []
    for i in text.lower():
        if i.isalpha():
            l.append(d[i])
    answer = ' '.join([str(i) for i in l])        
    return answer           
```