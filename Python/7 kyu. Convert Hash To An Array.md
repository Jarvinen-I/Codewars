# Convert Hash To An Array

Convert a hash into an array. Nothing more, Nothing less.
```
{name: 'Jeremy', age: 24, role: 'Software Engineer'}
```
should be converted into
```
[["age", 24], ["name", "Jeremy"], ["role", "Software Engineer"]]
```
Note: The output array should be sorted alphabetically by key name.

Good Luck!

# Solution
```
def convert_hash_to_array(hash):
    new_list = []
    for key, value in hash.items():
        new_list.append([key, value])
    new_list = sorted(new_list)   
    return new_list
```