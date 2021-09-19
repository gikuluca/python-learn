#### Escape Characters
```py
spam = 'Say hi to Bob\' mother'
```
| Escape character | Print as |
| :-----------: | :------: |
| \' | Character escape |
| \t | Tab |
| \n | New line |
| \\ | Back slash|

#### Row strings 
A row string completely ignores all escape characters and prints any backslash that apears in the string.
```py
print(r'That is Carol\'s cat.') # 'That is Carol\'s cat'
```
#### Multiline comments
```py
""" This is a test Python progma 
asd
asd
asd
"""
def spam():
  """ this is a multiline comment to help 
  explain what multiline comment looks like"""
  print("hello")
```
#### String inside Strings
```py
'My name is %s. I am %s years old.' %(name,age)
f'My name is {name}. I am {age} years old.'
```
