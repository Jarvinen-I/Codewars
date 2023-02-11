# Break camelCase

Complete the solution so that the function will break up camel casing, using a space between words.

### Example
```
"camelCasing"  =>  "camel Casing"
"identifier"   =>  "identifier"
""             =>  ""
```

# Solution
```
def solution(s):
    lst = []
    for i in range(len(s)):
        if s[i].isupper():
            lst.append(' ' + s[i])
        else:
            lst.append(s[i])
    return ''.join(lst)        
```