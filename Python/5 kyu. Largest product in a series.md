# Largest product in a series

Complete the ```greatestProduct``` method so that it'll find the greatest product of five consecutive digits in the given string of digits.

For example:
```
greatestProduct("123834539327238239583") // should return 3240
```
The input string always has more than five digits.

Adapted from Project Euler.

# Solution
```
def greatest_product(n):
    total = 1
    flag = False
    for i in range(len(n) - 4):
        count = int(n[i]) * int(n[i+1]) * int(n[i+2]) * int(n[i+3]) * int(n[i+4])
        if count > total:
            flag = True
            total = count
            
    return total if flag else 0
```