# Python Concepts from Module 1 — Reference Guide

A quick reference for the core Python concepts covered in Module 1 of the Google Cybersecurity Certificate: comments, functions, conditional statements, and iterative statements.

## Comments

| Syntax | Description | Example |
| --- | --- | --- |
| `#` | Starts a line containing a Python comment | `# Print approved usernames` |

A comment is a note a programmer makes about the intention behind their code. Python ignores everything after `#` on that line.

## Functions

| Function | Description | Example | Result |
| --- | --- | --- | --- |
| `print()` | Outputs a specified object to the screen | `print("login success")` | Displays `login success` |
| | | `print(9 < 7)` | Displays `False` |
| `type()` | Returns the data type of its input | `print(type(51.1))` | Returns `float` |
| | | `print(type(True))` | Returns `bool` |
| `range()` | Generates a sequence of numbers | `range(0, 5, 1)` | Sequence `0, 1, 2, 3, 4` |
| | | `range(5)` | Sequence `0, 1, 2, 3, 4` |

Notes on `range()`:
- The start point is inclusive; the stop point is exclusive.
- If the start point is omitted, it defaults to 0.
- If the increment is omitted, it defaults to 1.

## Conditional statements

| Keyword / operator | Description | Example |
| --- | --- | --- |
| `if` | Starts a conditional statement | `if device_id != "la858zn":` |
| | Membership check | `if user in approved_list:` |
| `elif` | Evaluated only when previous conditions are `False` | `elif status == 500:` |
| `else` | Runs when all preceding conditions are `False` | `else:` |
| `and` | Both conditions must be `True` | `if username == "bmoreno" and login_attempts < 5:` |
| `or` | Only one condition needs to be `True` | `if status == 100 or status == 102:` |
| `not` | Negates a condition | `if not account_status == "removed":` |

## Iterative statements

| Keyword | Description | Example |
| --- | --- | --- |
| `for` | Begins a `for` loop that iterates through a sequence | `for username in ["bmoreno", "tshah", "elarson"]:` |
| | Iterate over a numeric sequence | `for i in range(10):` |
| `while` | Begins a `while` loop that iterates based on a condition | `while login_attempts < 5:` |
| `break` | Breaks out of a loop | `break` |
| `continue` | Skips the current iteration and continues with the next | `continue` |

## Summary

- **Comments** (`#`) document intent and are ignored at runtime.
- **Functions** such as `print()`, `type()`, and `range()` perform common tasks.
- **Conditional statements** (`if`, `elif`, `else`) with operators (`and`, `or`, `not`, `in`) control which code runs.
- **Iterative statements** (`for`, `while`) repeat code, with `break` and `continue` adjusting loop flow.
