# Micro Optimization: Digit Sum

You wrote a program that can calculate the sum of all the digits of a non-negative integer.

However, it's not fast enough. Can you make it faster?

### Input size
Python:

* 50 random tests of ```n <= 2^64```
* 50 random tests of ```n <= 2^120000```

# Solution
```
"""
# this is not fast enough!
def digit_sum(n):
    sum = 0
    while n > 9:
        sum += n % 10
        n //= 10
    return sum + n

# this is even worse
def digit_sum(n):
    return n if n<9 else n%10 + digit_sum(n//10)
"""

def digit_sum(n):
    return sum([int(i) for i in str(n)]) 
```