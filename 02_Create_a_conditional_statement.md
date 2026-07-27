# Create a Conditional Statement

Practice writing conditional statements in Python to automate security checks.

## Scenario

A security analyst first checks whether a user's operating system requires an update, then investigates login attempts to a specific device: whether the attempts were made by approved users and whether they occurred during organisation hours.

## Concepts covered

- `if`, `elif`, and `else` statements
- Comparison operators (`==`)
- Logical operators (`and`, `or`)
- The `in` operator for membership checks
- Boolean variables in conditions

## Tasks

### Task 1: Check for an up-to-date operating system

```python
system = "OS 2"

if system == "OS 2":
    print("no update needed")
```

Output: `no update needed`

### Task 2: Observe behaviour with a different value

```python
system = "OS 1"

if system == "OS 2":
    print("no update needed")
```

Nothing is displayed, because the condition evaluates to `False`.

### Task 3: Add an alternative message with `else`

```python
system = "OS 1"

if system == "OS 2":
    print("no update needed")
else:
    print("update needed")
```

Output: `update needed`

### Task 4: Handle each operating system with `elif`

```python
system = "OS 2"

if system == "OS 2":
    print("no update needed")
elif system == "OS 1":
    print("update needed")
elif system == "OS 3":
    print("update needed")
```

Output: `no update needed`

This version only displays a message for the three recognised operating systems, rather than defaulting to "update needed" for any other input.

### Task 5: Combine conditions concisely with `or`

```python
system = "OS 2"

if system == "OS 2":
    print("no update needed")
elif system == "OS 1" or system == "OS 3":
    print("update needed")
```

Output: `no update needed`

> Note: each side of `or` must be a complete comparison. Writing `elif system == "OS 1" or "OS 3":` is a common mistake, because the string `"OS 3"` on its own always evaluates as truthy.

### Task 6: Compare a username against two approved users

```python
approved_user1 = "elarson"
approved_user2 = "bmoreno"
username = "bmoreno"

if username == approved_user1 or username == approved_user2:
    print("This user has access to this device.")
else:
    print("This user does not have access to this device.")
```

Output: `This user has access to this device.`

### Task 7: Use an allow list with the `in` operator

```python
approved_list = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab"]
username = "bmoreno"

if username in approved_list:
    print("This user has access to this device.")
else:
    print("This user does not have access to this device.")
```

Output: `This user has access to this device.`

### Task 8: Check login time with a Boolean variable

```python
organization_hours = True

if organization_hours == True:
    print("Login attempt made during organization hours.")
else:
    print("Login attempt made outside of organization hours.")
```

Output: `Login attempt made during organization hours.`

### Task 9: Assemble both checks

```python
approved_list = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab"]
username = "bmoreno"

if username in approved_list:
    print("This user has access to this device.")
else:
    print("This user does not have access to this device.")

organization_hours = True

if organization_hours == True:
    print("Login attempt made during organization hours.")
else:
    print("Login attempt made outside of organization hours.")
```

Output:
```
This user has access to this device.
Login attempt made during organization hours.
```

### Task 10: Combine both conditions into one statement

```python
approved_list = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab"]
username = "bmoreno"
organization_hours = True

if username in approved_list and organization_hours == True:
    print("Login attempt made by an approved user during organization hours.")
else:
    print("Username not approved or login attempt made outside of organization hours.")
```

Output: `Login attempt made by an approved user during organization hours.`

## Key takeaways

- `if`, `elif`, and `else` let code respond to different conditions.
- The `in` operator provides a concise way to check membership in a list, which scales better than comparing against many individual variables.
- The `and` operator requires both conditions to be `True`; the `or` operator requires only one.
- Combining conditions with logical operators produces more concise, readable code.
