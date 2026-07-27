# Create Loops

Practice writing iterative statements in Python to automate repetitive security tasks.

## Scenario

A security analyst writes programs to automate displaying messages about network connection attempts, detecting IP addresses attempting to access restricted data, and generating employee ID numbers for a Sales department.

## Concepts covered

- `for` loops with `range()`
- `while` loops
- Loop variables
- Iterating over a list
- `if`/`else` inside a loop
- The `break` keyword

## Tasks

### Task 1: Repeat a message with a `for` loop

```python
for i in range(3):
    print("Connection could not be established.")
```

Output:
```
Connection could not be established.
Connection could not be established.
Connection could not be established.
```

### Task 2: Drive the loop with a variable

```python
connection_attempts = 3

for i in range(connection_attempts):
    print("Connection could not be established.")
```

Output:
```
Connection could not be established.
Connection could not be established.
Connection could not be established.
```

Changing the value of `connection_attempts` changes how many times the message is displayed.

### Task 3: Achieve the same result with a `while` loop

```python
connection_attempts = 0

while connection_attempts < 3:
    print("Connection could not be established.")
    connection_attempts = connection_attempts + 1
```

Output:
```
Connection could not be established.
Connection could not be established.
Connection could not be established.
```

**Difference between the loops:** a `for` loop terminates after a set number of iterations, while a `while` loop terminates once a condition is no longer met. In a `while` loop the loop variable is initialised beforehand and updated inside the loop body; in a `for` loop the sequence and increment are defined in the loop header. When you do not know in advance how many iterations are needed, a `while` loop is the better fit.

### Task 4: Iterate over a list of IP addresses

```python
ip_addresses = ["192.168.142.245", "192.168.109.50", "192.168.86.232",
                "192.168.131.147", "192.168.205.12", "192.168.200.48"]

for i in ip_addresses:
    print(i)
```

Output:
```
192.168.142.245
192.168.109.50
192.168.86.232
192.168.131.147
192.168.205.12
192.168.200.48
```

### Task 5: Check each IP against an allow list

```python
allow_list = ["192.168.243.140", "192.168.205.12", "192.168.151.162", "192.168.178.71",
              "192.168.86.232", "192.168.3.24", "192.168.170.243", "192.168.119.173"]

ip_addresses = ["192.168.142.245", "192.168.109.50", "192.168.86.232",
                "192.168.131.147", "192.168.205.12", "192.168.200.48"]

for ip in ip_addresses:
    if ip in allow_list:
        print("IP address is allowed")
    else:
        print("IP address is not allowed")
```

Output:
```
IP address is not allowed
IP address is not allowed
IP address is allowed
IP address is not allowed
IP address is allowed
IP address is not allowed
```

### Task 6: Terminate the loop with `break`

```python
allow_list = ["192.168.243.140", "192.168.205.12", "192.168.151.162", "192.168.178.71",
              "192.168.86.232", "192.168.3.24", "192.168.170.243", "192.168.119.173"]

ip_addresses = ["192.168.142.245", "192.168.109.50", "192.168.86.232",
                "192.168.131.147", "192.168.205.12", "192.168.200.48"]

for ip in ip_addresses:
    if ip in allow_list:
        print("IP address is allowed")
    else:
        print("IP address is not allowed. Further investigation of login activity required")
        break
```

Output:
```
IP address is not allowed. Further investigation of login activity required
```

The loop stops as soon as it encounters an IP address outside the allow list.

### Task 7: Generate employee IDs with a `while` loop

Employee IDs must be unique, divisible by 5, and fall between 5000 and 5150 (inclusive).

```python
i = 5000

while i <= 5150:
    print(i)
    i = i + 5
```

Output: `5000, 5005, 5010, ... 5145, 5150` (each on its own line).

### Task 8: Add an alert once the loop reaches 5100

```python
i = 5000

while i <= 5150:
    print(i)
    if i == 5100:
        print("Only 10 valid employee ids remaining")
    i = i + 5
```

Output includes the alert immediately after `5100` is printed.

> `print(i)` is placed before the conditional so that the current ID is always displayed each iteration, and the alert check then runs against that same value.

## Key takeaways

- `for` loops repeat a fixed number of times; `while` loops repeat until a condition changes.
- `range()` can take a literal number or a variable to control iteration count.
- Looping over a list processes one element per iteration.
- `break` exits a loop early, which is useful for stopping on a detected anomaly.
- The order of statements inside a loop determines what is displayed and when.
