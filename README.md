# python-learn


#### defaultdict
A defaultdict will never raise a KeyError. Any key that does not exist gets the default value returned.
```py
state_capitals = {
'Arkansas': 'Little Rock',
'Colorado': 'Denver',
'California': 'Sacramento',
'Georgia': 'Atlanta'
}
```
If we try to access a non-existent key, python returns us an error as follows
```py
state_capitals['Alabama']
Traceback (most recent call last):
File "<ipython-input-61-236329695e6f>", line 1, in <module>
state_capitals['Alabama']
KeyError: 'Alabama'
```
Let us try with a defaultdict. It can be found in the collections module.
```py
from collections import defaultdict
state_capitals = defaultdict(lambda: 'Boston')
```
If we try to access the dict with a non-existent key, python will return us the default value i.e. Boston
 ```py
state_capitals['Alabama']
'Boston'
```

## User input

Python 3.x Version ≥ 3.0
```py
name = input("What is your name? ")
# Out: What is your name? _
```

## Built in Module and Functions 

```py 
pow(2,3)
#or
dir(__builtins__)
[
'ArithmeticError',
'AssertionError',
'AttributeError',
'BaseException',
'BufferError',
'BytesWarning',
'DeprecationWarning',
'EOFError',
'Ellipsis',
'EnvironmentError',
'Exception',
'False',
'FloatingPointError',
'FutureWarning',
'GeneratorExit',
'IOError',
'ImportError',
'ImportWarning',
'IndentationError',
'IndexError',
'KeyError',
'KeyboardInterrupt',
'LookupError',
'MemoryError',
'NameError',
'None',
'NotImplemented',
'NotImplementedError',
'OSError',
'OverflowError',
'PendingDeprecationWarning',
'ReferenceError',
'RuntimeError',
'RuntimeWarning',
'StandardError',
'StopIteration',
'SyntaxError',
'SyntaxWarning',
'SystemError',
'SystemExit',
'TabError',
'True',
'TypeError',
'UnboundLocalError',
'UnicodeDecodeError',
'UnicodeEncodeError',
'UnicodeError',
'pow',
'print',
'property',
'quit',
'range',
'raw_input',
'reduce',
'reload',
'repr',
'reversed',
'round',
'set',
'setattr',
'slice',
'sorted',
'staticmethod',
'str',
'sum',
'super',
'tuple',
'type',
'unichr',
'unicode',
'vars',
'xrange',
'zip'
]
```
To know the functionality of any function, we can use built in function help .
```py
help(max)
Help on built-in function max in module __builtin__:
max(...)
max(iterable[, key=func]) -> value
max(a, b, c, ...[, key=func]) -> value
...
```

## Creating a module
A module can be created by creating a .py file.
```py
# hello.py
def say_hello():
print("Hello!")
```
Functions in a module can be used by importing the module.
For modules that you have made, they will need to be in the same directory as the file that you are importing them
into. (However, you can also put them into the Python lib directory with the pre-included modules, but should be
avoided if possible.)
```py
$ python
 import hello
 hello.say_hello()
=> "Hello!"
```
Modules can be imported by other modules.
```py
# greet.py
import hello
hello.say_hello()
```
Specific functions of a module can be imported.
```py
# greet.py
from hello import say_hello
say_hello()
```


### String function - str() and repr()
There are two functions that can be used to obtain a readable representation of an object.
repr(x) calls x.__repr__(): a representation of x. eval will usually convert the result of this function back to the
original object.
str(x) calls x.__str__(): a human-readable string that describes the object. This may elide some technical detail.


chapter 4
