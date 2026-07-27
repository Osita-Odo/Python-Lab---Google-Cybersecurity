# Create More Functions

Use built-in functions to prepare a list of failed login attempts for analysis, and build up a user-defined function that compares a user's current-day logins against their average.

## Scenario

A security analyst works with a list containing the number of failed login attempts per month to identify patterns that might indicate malicious activity, and defines a function that compares a user's current-day logins to an average, improving it step by step with a return statement.

## Concepts covered

- Built-in functions `sorted()` and `max()`
- Defining functions with parameters
- Adding parameters incrementally
- Calculations inside functions
- The `return` statement
- Using a returned value in a conditional

## Tasks

### Task 1: Sort the failed login list

```python
failed_login_list = [119, 101, 99, 91, 92, 105, 108, 85, 88, 90, 264, 223]
print(sorted(failed_login_list))
```

Output: `[85, 88, 90, 91, 92, 99, 101, 105, 108, 119, 223, 264]`

Sorting reveals two outliers (223 and 264) that stand well above the rest.

### Task 2: Find the maximum

```python
failed_login_list = [119, 101, 99, 91, 92, 105, 108, 85, 88, 90, 264, 223]
print(max(failed_login_list))
```

Output: `264`

### Task 3: Define a function with two parameters

```python
def analyze_logins(username, current_day_logins):
    print("Current day login total for", username, "is", current_day_logins)
```

> The function header must end with a colon (`:`); omitting it raises a `SyntaxError`.

### Task 4: Call the function

```python
def analyze_logins(username, current_day_logins):
    print("Current day login total for", username, "is", current_day_logins)

analyze_logins("ejones", 9)
```

Output: `Current day login total for ejones is 9`

### Task 5: Add a third parameter

```python
def analyze_logins(username, current_day_logins, average_day_logins):
    print("Current day login total for", username, "is", current_day_logins)
    print("Average logins per day for", username, "is", average_day_logins)

analyze_logins("ejones", 9, 3)
```

Output:
```
Current day login total for ejones is 9
Average logins per day for ejones is 3
```

### Task 6: Calculate a login ratio

```python
def analyze_logins(username, current_day_logins, average_day_logins):
    print("Current day login total for", username, "is", current_day_logins)
    print("Average logins per day for", username, "is", average_day_logins)
    login_ratio = current_day_logins / average_day_logins
    print(username, "logged in", login_ratio, "times as much as they do on an average day.")

analyze_logins("ejones", 9, 3)
```

Output:
```
Current day login total for ejones is 9
Average logins per day for ejones is 3
ejones logged in 3.0 times as much as they do on an average day.
```

> If `average_day_logins` were 0, dividing would raise `ZeroDivisionError`. This activity assumes every user has logged in at least once, so the average is always greater than 0.

### Task 7: Return the ratio

```python
def analyze_logins(username, current_day_logins, average_day_logins):
    print("Current day login total for", username, "is", current_day_logins)
    print("Average logins per day for", username, "is", average_day_logins)
    login_ratio = current_day_logins / average_day_logins
    return login_ratio

login_analysis = analyze_logins("ejones", 9, 3)
print(login_analysis)
```

Output:
```
Current day login total for ejones is 9
Average logins per day for ejones is 3
3.0
```

`return` sends the value back to the caller so it can be stored and reused.

### Task 8: Use the returned value in a conditional

```python
def analyze_logins(username, current_day_logins, average_day_logins):
    print("Current day login total for", username, "is", current_day_logins)
    print("Average logins per day for", username, "is", average_day_logins)
    login_ratio = current_day_logins / average_day_logins
    return login_ratio

login_analysis = analyze_logins("ejones", 9, 3)

if login_analysis >= 3:
    print("Alert! This account has more login activity than normal.")
```

Output:
```
Current day login total for ejones is 9
Average logins per day for ejones is 3
Alert! This account has more login activity than normal.
```

## Key takeaways

- `sorted()` and `max()` are built-in functions that help spot anomalies in data.
- Functions can be extended by adding parameters and calculations over time.
- `return` sends a result back to the caller, unlike `print()`, which only displays it.
- A returned value can be stored in a variable and reused, for example in a conditional that raises an alert.
