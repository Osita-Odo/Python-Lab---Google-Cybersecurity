# Define and Call a Function

Practice defining and calling functions in Python to reuse blocks of code.

## Scenario

A security analyst defines and calls a function that displays an alert about a potential security issue, then works with a list of employee usernames, creating a function that converts the list into a single string.

## Concepts covered

- Defining functions with `def`
- Calling functions
- Including a `for` loop inside a function
- String concatenation to build output
- Formatting output for readability

## Tasks

### Task 1: Analyse a function definition

```python
def alert():
    print("Potential security issue. Investigate further.")
```

`def alert():` defines a reusable block of code named `alert`. Its body displays the message when the function is called. Defining the function alone produces no output.

### Task 2: Call the function

```python
def alert():
    print("Potential security issue. Investigate further.")

alert()
```

Output: `Potential security issue. Investigate further.`

Placing code in a function lets it be reused whenever needed, rather than rewriting it.

### Task 3: Add a `for` loop inside the function

```python
def alert():
    for i in range(3):
        print("Potential security issue. Investigate further.")

alert()
```

Output:
```
Potential security issue. Investigate further.
Potential security issue. Investigate further.
Potential security issue. Investigate further.
```

### Task 4: Write a function header

```python
def list_to_string():
```

This header alone raises an error, because a function requires a body. The body is completed in later tasks.

### Task 5: Loop through the list inside the function

```python
def list_to_string():
    username_list = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab",
                     "gesparza", "alevitsk", "wjaffrey"]
    for i in username_list:
        print(i)

list_to_string()
```

Output: each username on its own line.

### Task 6: Concatenate the usernames into one string

```python
def list_to_string():
    username_list = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab",
                     "gesparza", "alevitsk", "wjaffrey"]
    sum_variable = ""
    for i in username_list:
        sum_variable = sum_variable + i
    print(sum_variable)

list_to_string()
```

Output: `elarsonbmorenotshahsgilmoreeraabgesparzaalevitskwjaffrey`

Placing `print(sum_variable)` outside the loop displays the final combined string once.

### Task 7: Add a comma and space between usernames

```python
def list_to_string():
    username_list = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab",
                     "gesparza", "alevitsk", "wjaffrey"]
    sum_variable = ""
    for i in username_list:
        sum_variable = sum_variable + i + ", "
    print(sum_variable)

list_to_string()
```

Output: `elarson, bmoreno, tshah, sgilmore, eraab, gesparza, alevitsk, wjaffrey, `

## Key takeaways

- Functions are defined with `def` and run only when called.
- Functions can contain other constructs, such as `for` loops.
- String concatenation (`+`) builds a single string from list elements.
- Adding separators such as `", "` improves the readability of combined output.
