# Assign Python Variables

Practice assigning values to variables and determining their data types, in the context of automating the analysis of login attempts to a device.

## Scenario

A security analyst writes code to automate analysis of login attempts made to a specific device. The first step is creating variables to track information relevant to the login process: the device ID, a list of approved usernames, the maximum login attempts allowed per user, the current login attempts made by a user, and the login status.

## Concepts covered

- Assigning values to variables with the `=` operator
- Checking data types with `type()`
- String, list, integer, and Boolean data types
- Reassigning variables
- Comparison operators (`<=`)
- Displaying output with `print()`

## Tasks

### Task 1: Assign and display the device ID

```python
device_id = "72e08x0"
print(device_id)
```

Output: `72e08x0`

### Task 2: Find the data type of the device ID

```python
device_id = "72e08x0"
device_id_type = type(device_id)
print(device_id_type)
```

Output: `<class 'str'>`

### Task 3: Create a list of approved usernames

```python
username_list = ["madebowa", "jnguyen", "tbecker", "nhersh", "redwards"]
print(username_list)
```

Output: `['madebowa', 'jnguyen', 'tbecker', 'nhersh', 'redwards']`

### Task 4: Find the data type of the username list

```python
username_list = ["madebowa", "jnguyen", "tbecker", "nhersh", "redwards"]
username_list_type = type(username_list)
print(username_list_type)
```

Output: `<class 'list'>`

### Task 5: Reassign the username list to an updated version

```python
username_list = ["madebowa", "jnguyen", "tbecker", "nhersh", "redwards"]
print(username_list)

username_list = ["madebowa", "jnguyen", "tbecker", "nhersh", "redwards", "lpope"]
print(username_list)
```

Output:
```
['madebowa', 'jnguyen', 'tbecker', 'nhersh', 'redwards']
['madebowa', 'jnguyen', 'tbecker', 'nhersh', 'redwards', 'lpope']
```

### Task 6: Assign the maximum login attempts

```python
max_logins = 3
max_logins_type = type(max_logins)
print(max_logins_type)
```

Output: `<class 'int'>`

### Task 7: Assign the current login attempts

```python
login_attempts = 2
login_attempts_type = type(login_attempts)
print(login_attempts_type)
```

Output: `<class 'int'>`

### Task 8: Compare current attempts against the maximum

```python
max_logins = 3
login_attempts = 2
print(login_attempts <= max_logins)
```

Output: `True` (the number of login attempts is less than or equal to the maximum allowed)

### Task 9: Observe the comparison with a higher value

```python
max_logins = 3
login_attempts = 5
print(login_attempts <= max_logins)
```

Output: `False` (the number of login attempts exceeds the maximum allowed)

### Task 10: Assign a Boolean login status

```python
login_status = False
login_status_type = type(login_status)
print(login_status_type)
```

Output: `<class 'bool'>`

## Key takeaways

- Variables are assigned with the `=` operator and can be reassigned to new values at any point.
- The `type()` function returns the data type of a value: `str`, `list`, `int`, or `bool`.
- Boolean values (`True`, `False`) are written without quotation marks.
- Comparison operators such as `<=` return Boolean results.
- Small details, such as casing, matter: a minor mistake can stop code from running.
