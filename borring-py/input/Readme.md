# Input validation

```py
input() # return str type
```
```py
import pyinputplus
inputNum() # ensure that the user enters a number an returns an int
inputStr() # ensure that the user enters a str an returns a str
inputChoice() #Ensure that user  enters one of the provided choices
inputMenu()
inputDatetime()
inputYesNo()
```
Example:
```py
>>> import pyinputplus as puip 
>>> response = puip.inputNum('Entern num: ', min=4)
Entern num: 3
Number must be at minimum 4.
Entern num: 4
```

