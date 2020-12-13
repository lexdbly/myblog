---
title: "Retrieve Dictionary Keys from Values in Python"
date: 2020-12-13
tags:
    - python
    - dictionary
categories:
    - tech
keywords:
    - python
    - dictionary
draft: false
---

Standard way of using a dictionary is providing keys to retrieve values.

Lets create a dictonary of colors

```python
>>> colors = {"red": 1, "black": 2, "blue": 3}
```

Retrieving dictionary item value via key
```python
>>> print(colors["red"])
1
>>> print(colors["blue"])
3
```

In order to retrieve a key by using value, we need to use two lists:
- A list of keys
- A list of values

Then we need to index them

```python
colors = {"red": 1, "black": 2, "blue": 3}
keylist = list(colors.keys()) # list of keys
valuelist = list(colors.values()) # list of values

colorvalue = 3 # assigning known value to colorvalue variable
colorkey = keylist[valuelist.index(colorvalue)] # retrieving key by using keylist and valuelist together

>>> print(colorkey)
"blue"
```

Above code gets the index of known value in the value list. In this case, index number of the value 3 is 2.

Then searching placing the index number in keylist. Value of the index = 2 in the key list is "blue".

This is pretty much matching the locations of items in two separate list, which are in fact directly correlated in a dictionary.