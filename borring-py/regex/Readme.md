```py
import re

phoneNumRegex = re.compile(r'\d\d\d-\d\d\d')
mo = phoneNumRegex.search('My number is 411-555')
print( f'Phone: {mo.group()}') # 'Phone: 411-555'
```

#### Grouping with parantheses
```py
phoneNumRegex = re.compile(r'(\d\d\d)-(\d\d\d)')
mo = phoneNumRegex.search('My numb is 415-555.')
mo.group(1) # 415
mo.group(2) # 555
mo.group(0) # 415-555
mo.group()  # 415-555
mo.groups() #  ('415','555')
```
#### The findall()
search() will return a Match object of the first matched text in the searched string
the findall() will return the strings of every match in the searched stringa and will return a list with them.

| Shothand character class | Reperesnts |
| :-----------: | :-------: |
| \d | Any numeric digit from 0 to 9 |
| \D | not \d |
| \w | Any letter, numeric digit, undersocre |
| \W | not \w |
| \s | Any space, tab or newline |
| \S | not \s |
| ^spam | at the beggining of string |
| spam$ | at the end of string
| [abc] | matches any char between the brackets |
| [^abc] | matches any char that isn't between the brackets |

#### Case-insensitive Matching
'''py
robocop = re.compile(r'robocoP', re.I) # re.I or re.U second argument to the compile 
```
#### Substituting strings 
```py 
namesRegex = re.compile(r'Agent \w+')
namesRegex.sub('Censored', 'Agent Alice gave the secret documents to Agent Bob.')
# 'Censored gave the secret documents to Censored'
```

