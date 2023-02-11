# Convert string to camel case

Complete the method/function so that it converts dash/underscore delimited words into camel casing. The first word within the output should be capitalized only if the original word was capitalized (known as Upper Camel Case, also often referred to as Pascal case). The next words should be always capitalized.

### Examples

```"the-stealth-warrior"``` gets converted to ```"theStealthWarrior"```
"The_Stealth_Warrior"``` gets converted to ```"TheStealthWarrior"```
```

# Solution
```
def to_camel_case(text):
    if text == '':
        return '' 
    camel = []
    s = ['-', '_']
    
    camel.append(text[0])
        
    for i in range(1, len(text)):
        if text[i] in s:
            camel.append('')
        elif text[i-1] in s:
            camel.append(text[i].upper())
        else:
            camel.append(text[i])
    return ''.join(camel) 
```