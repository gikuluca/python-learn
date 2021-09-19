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

### Dictionaries
Dictionaries are mutable 
items in Dictionaries are unordered. While the order of itmes matters for determining whether tho list are the same. So we cannot compare 2 dictonaries
Example:
```py
spam = ['a,'b','c']
bacon = ['d,'e','f']
spam == bacon
False

eggs = {'a':1,'b':2}
ham = {'c':1,'d':3}
eggs == ham
True
```

#### Dictionaries methods
```py
spam {'color':'red', 'age': 42}
for v in spam.values():
  print(v)

red
42

for k in spam.keys():
  print(k)

color
age

for i in spam.items():
  print(i)
('color','red')
('age',42)
```
If you want a true list from one of these methods, pass its list-like return
value to the list() function:
```py
spam.keys() #dict_keys(['color','age'])
list(spam.keys()) #['color','age']
```
Trick
```py
for k,v in spam.items():
  print(k+' '+v)
# age 42
# color red
```
#### Checking Whether a key or value exists in a dict
```py
'color' in spam.keys() # True
'False' in spam.values() #False
```
### THe get() Method
```py
p = {'apples':5, 'cup':2}
'I am bringing '+ str(p.get('cup',0))+ ' cups.' # 'I am bringing 2 cups.'
'I am bringing '+ str(p.get('eggs',0))+ ' eggs.' # 'I am gringing 0 eggs.'
```
Because there is no 'eggs' key in the p dictionary, the default value 0 is returned. Whitout using get(), the caude would have caused am error message : KeyError:'eggs'

