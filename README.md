# Effective Python Notes

## Chapter 1: Pythonic Thinking
### Item 1: Know Which Version of Python You're Using
```
$ python --version
```
Prefer Python3 as it's the primary focus of Python community.
### Item 2: Follow the PEP8 Style Guide
Tools like `pylint` and `flake8` are available for PEP8 style guide checking

### Item 3: Know the Differences Between bytes, str, and unicode
- In Python 3, `bytes` are sequences of 8-bit values and `str` are sequences of Unicode characters.
- In Python 2, `str` are sequences of 8-bit values, and `unicode` are sequences of Unicode characters.
- In Python 2, `unicode` and `str` can be used together sometimes, while in Python 3, `bytes` and `str` can't be used together.

### Item 4: Write Helper Functions Instead of Complex Expressions
Python has a lot of cool syntax features. You can write complex expressions in one-line, but that doesn't mean you should. Using helper functions can make your code more understandable.
For example:
```python
values = {'red': ['4', '3'], 'green': [''], 'blue': ['2']}
# print first int of list or 0 if list is empty or if key does not exist.
colors = ['red', 'green', 'blue', 'mauve']
for key in colors:
    print(int(values.get(key, [''])[0] or 0))
 ```
 if less ideal than
 ```python
 for key in colors:
    print(get_first_int(values, key)
    
 def get_first_int(values, key, default=0):
    found = values.get(key, [''])
    if found[0]:
      found = int(found[0])
    else:
      found=default
    return found
  ```
