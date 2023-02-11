# Simple Fun #52: Pair Of Shoes

### Task
Yesterday you found some shoes in your room. Each shoe is described by two values:
```
type indicates if it's a left or a right shoe;
size is the size of the shoe.
```
Your task is to check whether it is possible to pair the shoes you found in such a way that each pair consists of a right and a left shoe of an equal size.

### Example
For:
```
shoes = [[0, 21], 
         [1, 23], 
         [1, 21], 
         [0, 23]]
```
the output should be ```true```;

For:
```
shoes = [[0, 21], 
         [1, 23], 
         [1, 21], 
         [1, 23]]
```
the output should be ```false```.

### Input/Output
* ```[input]``` 2D integer array ```shoes```
Array of shoes. Each shoe is given in the format [type, size], where type is either 0 or 1 for left and right respectively, and size is a positive integer.

Constraints: ```2 ≤ shoes.length ≤ 50,  1 ≤ shoes[i][1] ≤ 100.```

* ```[output]``` a boolean value

```true``` if it is possible to pair the shoes, ```false``` otherwise.

# Solution
```
def pair_of_shoes(shoes):
    shoes = list(shoes)
    l = []
    for i in shoes:
        l.append(i[0])
        l.append(i[1])
    for i in l:
        if l.count(i) < 2:
            if i == 0 or i == 1:
                continue
            else:
                return False
    if 0 in l and 1 in l:
        if l.count(0) < l.count(1) or l.count(1) < l.count(0):
            return False
    for i in l:
        if l.count(i) > 2:
            if l.count(i) % 2 and i != 0 and i != 1:
                return False
    return True     
```