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
