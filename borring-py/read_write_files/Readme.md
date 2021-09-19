```py
from pathlib import Path
str(Path('s','b','e')) #'s\\b\\e' for Windows
                       # 's/b/e' for Unix
```

#### Getting parts of a file path

/home/al/spam.txt
/ -> anchor
home/al/ -> parent
spam.txt -> name 
spam -> stem
txt -> suffix

```py
>>> from pathlib import Path
>>> p = Path(r'/home/giku/asd.txt')
>>> p.name
'asd.txt'
>>> p.stem
'asd'
>>> p.anchor
'/'
```
#### File sizes and Folder COntents
```py>>> import os
>>> os.path.getsize('/home/giku/Documents')
4096
>>> os.listdir('/home/giku/Documents')
['MatLab', 'viber_telegram_phone_detection', 'zips', 'apktool', 'univ_terraform', 'dex2jar', 'docsLocation', 'jadx', 'heat-t', 'vpn_lyon1', 'SA_M1.zip', 'jenkins_v1', 'study', 'SA_M1', '.~lock.prof.csv#', 'nodejs', 'sources', 'SRE', 'GIT+ UNIV M2.zip', 'Oxygen', 'ldap', 'lib', 'M2SRIV', 'tpwifi', 'english', 'marcel', 'svs', 'Maftea', 'h4rpy', 'Docker', 'tmp', 'backup', 'jenkins', 'serverPython', 'etude_de_cas', 'git_training', 'WiFi', 'TheGate']
```

#### Opening Files with the open() Function

```py
hellofile = open(Path.home() / 'hello.txt')
```

#### Reading the  Contents of Files
```py 
helloContent = helloFile.read()
helloContent
'Hellom world'
```
or 
```
sonnetFile.readlines() -> will return a list with each line as element of it
```

#### Writing to Files
```py
bFile = open('bacon.txt','w')
bFile.write('Hello, world!\n')
13
bFile.close()
bFile = open('bacon.txt','a')
bFile.write('Bacon is not a vegetable.')
25
bFile.close()
bFile = open('bacon.txt')
content = baconFile.read()
print(content)
Hello, world!
Bacon is not a vegetable.
```
#### Saving Variables with the shelve Module

You can save variables in your Python programs to binary shelf files using the shelve module.
```py
>>> import shelve
>>> shelfile = shelve.open('mydata')
>>> cats = ['z','p','s']
>>> shelfile['cats'] = cats
>>> shelfile.close()
```
or  Saving variables with pprint.pformat()


