---
title: "How to list directory in Python 3"
date: 2021-07-09T17:13:27+01:00
---
Sometimes, we need to list all directories in a certain path. 
This simple task can be done in a few different ways:

### Using `os.listdir()`
```import os

open("/tmp/test.txt", 'a') # lets create a blank file

arr = os.listdir("/tmp")
print(arr)
```
It needs only one parameter, the path we want to list.

### Using `glob.glob()`
```import glob

open("/tmp/test.txt", 'a') # lets create a blank file

arr = glob.glob("/tmp/*.txt")
print(arr)
```
Its use is basically the same as `listdir`.
> Note: `glob.glob()` also accepts wildcards.
