# Last

Find the last element of the given argument(s).

### Examples
```
last([1, 2, 3, 4]) ==>  4
last("xyz")        ==> "z"
last(1, 2, 3, 4)   ==>  4
```

# Solution
```
def last(*args):
    if type(args[-1]) is int:
        return args[-1]
    else: 
        return args[-1][-1]
```