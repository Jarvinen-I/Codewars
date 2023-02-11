# Rot13

ROT13 is a simple letter substitution cipher that replaces a letter with the letter 13 letters after it in the alphabet. ROT13 is an example of the Caesar cipher.

Create a function that takes a string and returns the string ciphered with Rot13. If there are numbers or special characters included in the string, they should be returned as they are. Only letters from the latin/english alphabet should be shifted, like in the original Rot13 "implementation".

Please note that using ```encode``` is considered cheating.

# Solution
```
def rot13(message):
    string = ''
    for i in message:
        if not i.isalpha():
            string += i
        else:
            rotated = ord(i) + 13
            if i.isupper():
                if rotated > 90:
                    rotated = 64 + rotated - 90
                    string += chr(rotated)
                else:
                    string += chr(rotated)
            elif i.islower():
                if rotated > 122:
                    rotated = 96 + rotated - 122
                    string += chr(rotated)
                else:
                    string += chr(rotated) 
    return string     
```