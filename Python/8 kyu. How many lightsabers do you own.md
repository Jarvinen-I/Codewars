# How many lightsabers do you own?

Inspired by the development team at Vooza, write the function that

* accepts the name of a programmer, and
* returns the number of lightsabers owned by that person.
The only person who owns lightsabers is Zach, by the way. He owns 18, which is an awesome number of lightsabers. Anyone else owns 0.

Note: your function should have a default parameter.

# Solution
```
def how_many_light_sabers_do_you_own(name=''):
    return 18 if 'Zach' in name else 0
```