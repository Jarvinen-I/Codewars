# String incrementer

Your job is to write a function which increments a string, to create a new string.

* If the string already ends with a number, the number should be incremented by 1.
* If the string does not end with a number. the number 1 should be appended to the new string.

### Examples:

```foo``` -> ```foo1```

```foobar23``` -> ```foobar24```

```foo0042``` -> ```foo0043```

```foo9``` -> ```foo10```

```foo099``` -> ```foo100```

Attention: If the number has leading zeros the amount of digits should be considered.

# Solution
```
def increment_string(string):
    if string.isalpha():
        return string + '1'
    elif string.isdigit():
        return str(int(string) + 1).zfill(len(string))
    elif string == '':
        return '1'
    else:       
        digits = []
        while string[-1].isdigit():
            digits.append(string[-1])
            string = string[:-1]
        digits = ''.join([i for i in digits[::-1]])
        digits = str(int(digits) + 1).zfill(len(digits))
        return string + digits 
```
