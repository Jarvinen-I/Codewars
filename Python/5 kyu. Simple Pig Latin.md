# Simple Pig Latin

Move the first letter of each word to the end of it, then add "ay" to the end of the word. Leave punctuation marks untouched.

### Examples
```
pig_it('Pig latin is cool') # igPay atinlay siay oolcay
pig_it('Hello world !')     # elloHay orldway !
```

# Solution
```
def pig_it(text):
    pig_latin = []
    for i in text.split():
        if i.isalpha():
            pig_latin.append(i[1:] + i[0] + 'ay')
        else:
            pig_latin.append(i)
    return ' '.join([i for i in pig_latin])      
```