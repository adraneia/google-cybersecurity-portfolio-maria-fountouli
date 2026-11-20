# Course 7: Automate Cybersecurity Tasks with Python

## Module 1: Introduction to Python
- Python is used in security for **automation**: log analysis, checking access lists, malware analysis, managing alerts.
- Interpreted language, readable syntax. Notebooks (Jupyter, Colab) for testing code.
- **Data types:** `str`, `int`, `float`, `bool`, `list`, `tuple`, `dict`, `set`.
- **Variables:** `device_id = "h32rb17"` · `type(device_id)` → `<class 'str'>`
- **Conditionals:**
```python
if status == 200:
    print("OK")
elif status == 404:
    print("Not found")
else:
    print("Other")
```
- **Loops:** `for` (iterate over a sequence or `range()`), `while` (runs until a condition is false), `break`, `continue`.

## Module 2: Write effective Python code
- **Functions:** `def alert(): ...` with **parameters**, **arguments** and **return**.
- **Built-in functions:** `print()`, `type()`, `len()`, `max()`, `min()`, `sorted()`, `str()`.
- **Global vs local variables.** Avoid reusing the same name.
- **Modules and libraries:** `import re`, `import csv`, `import glob`, `import os`, `import time`, `import datetime`. External: Beautiful Soup, NumPy.
- **Code readability:** PEP 8, comments with `#`, docstrings, correct indentation.

## Module 3: Strings and lists
- **Strings:** indexing `s[0]`, slicing `s[0:3]`, `.upper()`, `.lower()`, `.index()`.
- **Lists:** `append()`, `remove()`, `insert()`, `.index()`. Lists are mutable, strings aren't.
- **Algorithms:** step by step process to solve a problem (e.g. extract the first 3 digits of every IP address).
- **Regular expressions (`re`):**
```python
import re
re.findall(r"\d+\.\d+\.\d+\.\d+", log)   # find IP addresses
re.findall(r"\w+@\w+\.\w+", text)        # find emails
```
  `\w` = alphanumeric, `\d` = digit, `\s` = whitespace, `+` = one or more, `*` = zero or more, `{n}` = exactly n times.

## Module 4: Python in practice
- **Opening files:**
```python
with open("allow_list.txt", "r") as file:
    ip_addresses = file.read()
ip_addresses = ip_addresses.split()
```
  Modes: `"r"` read, `"w"` write (overwrites), `"a"` append.
- `.split()` turns a string into a list, `" ".join(list)` turns it back into a string.
- **Parsing logs:** read the file, split lines, filter for failed logins or certain users.
- **Debugging:** syntax errors, logic errors, exceptions. Use `print()` statements, debuggers, read the error message.
- Example task: update an allow list by removing IPs that are on a remove list (loop + `.remove()` + write back to file).
