# Highest and Lowest

In this little assignment you are given a string of space separated numbers, and have to return the highest and lowest number.

# Solution
```
def high_and_low(numbers):
    l = [int(i) for i in numbers.split()]
    high, low = max(l), min(l)
    high_and_low = str(high) + ' ' + str(low)
    return high_and_low
```