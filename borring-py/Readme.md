### multiple assignment trick
```py
cat = ["a", "b", "c"]
v1, v2, v3 = cat
```

### enumerate() with Lists
instand of  using the range(list(someList))
we can do
```py
supplies = ['a', 'b', 'c', 'd']
for index, item in enumerate (supplies):
  print('Index ' + str(index) + ' in supplies is + ' +item )  
  
Index 0 in supplies is + a
Index 1 in supplies is + b
Index 2 in supplies is + c
Index 3 in supplies is + d
```

### Random
#### Random choice

```py
>>> import random
>>> random.choise(supplies)
>>> random.choice(supplies)
'c'
```
#### Random shuffle
```py
>>> random.shuffle(supplies)
>>> supplies
['d', 'c', 'b', 'a']
```

### Method
A method is the same thing as a function, except it is "aclled on" a value. Each data type has its own set of methods. 
like for list:
```py 
supplies.index('a')
supplies.append('e')
supplies.insert(1, 'x') # ['a','x', 'b', 'c', 'd', 'e']
supplies.remove('x')
supplies.sort()
supplies.sort(reverse=True) # for reversed 
supplies.sort(key=str.lower)
```

### Mutable and immutable Data Types
A list value is a mutable data type: it can have values added. removed or changed. However a string is immutable, it cannot be changed.
tuples are immutable 
Example:
```py
>>> name = 'Hiku'
>>> name[0]='G'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object does not support item assignment
```



