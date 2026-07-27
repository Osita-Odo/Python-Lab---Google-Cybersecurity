# Work with Strings in Python

Practice creating and manipulating string data: an employee ID, a device ID, and a URL.

## Scenario

A security analyst writes programs to automate updating employee IDs, extracting characters from a device ID, and extracting components from a URL.

## Concepts covered

- Converting between data types with `str()`
- Measuring length with `len()`
- String concatenation with `+`
- Indexing and slicing with bracket notation
- Locating substrings with `.index()`

## Tasks

### Task 1: Convert an employee ID to a string

```python
employee_id = 4186
print(type(employee_id))

employee_id = str(employee_id)
print(type(employee_id))
```

Output:
```
<class 'int'>
<class 'str'>
```

### Task 2: Check the length of the employee ID

```python
employee_id = 4186
employee_id = str(employee_id)

if len(employee_id) < 5:
    print("This employee ID has less than five digits. It does not meet length requirements.")
```

Output: `This employee ID has less than five digits. It does not meet length requirements.`

### Task 3: Pad a four-digit ID to five characters

```python
employee_id = 4186
employee_id = str(employee_id)
print(employee_id)

if len(employee_id) < 5:
    employee_id = "E" + employee_id

print(employee_id)
```

Output:
```
4186
E4186
```

> The task asks for "E" to be concatenated in front of the ID, so `"E" + employee_id` places it at the start.

### Task 4: Extract a single character from a device ID

```python
device_id = "r262c36"
print(device_id[3])
```

Output: `2`

Index values start at 0, so index `3` corresponds to the fourth character.

### Task 5: Slice the first three characters

```python
device_id = "r262c36"
print(device_id[0:3])
```

Output: `r26`

The ending index is exclusive, so the slice includes indices 0, 1, and 2.

### Task 6: Extract the protocol from a URL

```python
url = "https://exampleURL1.com"
print(url[0:8])
```

Output: `https://`

`https://` is eight characters long.

### Task 7: Locate the domain extension

```python
url = "https://exampleURL1.com"
print(url.index(".com"))
```

Output: `19`

### Task 8: Store the index in a variable

```python
url = "https://exampleURL1.com"
ind = url.index(".com")
```

Running this cell produces no output; it stores the position of `.com` for reuse.

### Task 9: Extract the domain extension using the stored index

```python
url = "https://exampleURL1.com"
ind = url.index(".com")
print(url[ind:ind + 4])
```

Output: `.com`

Expressing the end index relative to the start (`ind + 4`, because `.com` is four characters long) makes the slice easy to reason about.

### Task 10: Extract the website name

```python
url = "https://exampleURL1.com"
ind = url.index(".com")
print(url[8:ind])
```

Output: `exampleURL1`

The website name starts at index 8 (right after `https://`) and ends where `.com` begins.

## Key takeaways

- `str()` converts other data types into strings.
- `len()` returns the length of a string.
- Concatenation with `+` merges strings.
- Bracket notation supports both single-character indexing (`s[i]`) and slicing (`s[start:end]`), where the end index is exclusive and indexing starts at 0.
- `.index()` returns the starting position of a substring, which can be stored and reused in slices.
