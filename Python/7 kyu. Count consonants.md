# Count consonants

Complete the function that takes a string of English-language text and returns the number of consonants in the string.

Consonants are all letters used to write English excluding the vowels ```a, e, i, o, u```.

# Solution
```
def consonant_count(s):
    vowels = ['a', 'e', 'i', 'o', 'u']  
    count = 0
    for i in s.lower():
        if i not in vowels and i.isalpha():
            count += 1
    return count 
```