# Moving Zeros To The End

Write an algorithm that takes an array and moves all of the zeros to the end, preserving the order of the other elements.
```
move_zeros([1, 0, 1, 2, 0, 1, 3]) # returns [1, 1, 2, 1, 3, 0, 0]
```

# Solution
```
def move_zeros(lst):
    not_zeros, zeros = [], []
    for i in lst:
        if i != 0:
            not_zeros.append(i)
        else:
            zeros.append(i)
    lst = not_zeros + zeros        
    return lst        
```