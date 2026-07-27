# Develop an Algorithm

Develop an algorithm that connects users to their assigned devices, verifying that a user is approved and has brought their assigned device.

## Scenario

A security analyst builds an algorithm that indicates whether a user is approved on the system and has brought their assigned device to the security team. Two synchronised lists are used: the user at index `n` in `approved_users` is assigned the device at index `n` in `approved_devices`.

## Concepts covered

- List indexing
- `.append()` and `.remove()` list methods
- `.index()` to find an element's position
- Linking two synchronised lists by shared index
- `if`, `elif`, `else` and the `and` logical operator
- Nested conditionals inside a function

## Tasks

### Task 1: Access elements by index

```python
approved_users = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab"]
approved_devices = ["8rp2k75", "hl0s5o1", "2ye3lzg", "4n482ts", "a307vir"]

print(approved_users[0])
print(approved_devices[0])
```

Output:
```
elarson
8rp2k75
```

The element at the same index in each list corresponds to the same user.

### Task 2: Add a new user and device with `.append()`

```python
approved_users = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab"]
approved_devices = ["8rp2k75", "hl0s5o1", "2ye3lzg", "4n482ts", "a307vir"]

new_user = "gesparza"
new_device = "3rcv4w6"

approved_users.append(new_user)
approved_devices.append(new_device)

print(approved_users)
print(approved_devices)
```

Output:
```
['elarson', 'bmoreno', 'tshah', 'sgilmore', 'eraab', 'gesparza']
['8rp2k75', 'hl0s5o1', '2ye3lzg', '4n482ts', 'a307vir', '3rcv4w6']
```

`.append()` adds the new element to the end of each list.

### Task 3: Remove a user and device with `.remove()`

```python
approved_users = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab", "gesparza"]
approved_devices = ["8rp2k75", "hl0s5o1", "2ye3lzg", "4n482ts", "a307vir", "3rcv4w6"]

removed_user = "tshah"
removed_device = "2ye3lzg"

approved_users.remove(removed_user)
approved_devices.remove(removed_device)

print(approved_users)
print(approved_devices)
```

Output:
```
['elarson', 'bmoreno', 'sgilmore', 'eraab', 'gesparza']
['8rp2k75', 'hl0s5o1', '4n482ts', 'a307vir', '3rcv4w6']
```

### Task 4: Check whether a username is approved

```python
approved_users = ["elarson", "bmoreno", "sgilmore", "eraab", "gesparza"]
username = "sgilmore"

if username in approved_users:
    print("The user", username, "is approved to access the system.")
else:
    print("The user", username, "is not approved to access the system.")
```

Output: `The user sgilmore is approved to access the system.`

### Task 5: Find a username's index

```python
approved_users = ["elarson", "bmoreno", "sgilmore", "eraab", "gesparza"]
username = "sgilmore"

ind = approved_users.index(username)
print(ind)
```

Output: `2` (the third position, since indexing starts at 0)

### Task 6: Link the index across lists

```python
approved_users = ["elarson", "bmoreno", "sgilmore", "eraab", "gesparza"]
approved_devices = ["8rp2k75", "hl0s5o1", "4n482ts", "a307vir", "3rcv4w6"]
username = "sgilmore"

ind = approved_users.index(username)
print(approved_devices[ind])
```

Output: `4n482ts`

Finding the index in one list and reusing it in the other retrieves the matching device.

### Task 7: Verify username and device together

```python
approved_users = ["elarson", "bmoreno", "sgilmore", "eraab", "gesparza"]
approved_devices = ["8rp2k75", "hl0s5o1", "4n482ts", "a307vir", "3rcv4w6"]
username = "sgilmore"
device_id = "4n482ts"

ind = approved_users.index(username)

if username in approved_users and device_id == approved_devices[ind]:
    print("The username", username, "is approved to access the system.")
    print(device_id, "is the assigned device for", username)
```

Output:
```
The username sgilmore is approved to access the system.
4n482ts is the assigned device for sgilmore
```

> Comparing `device_id` against `approved_devices[ind]` confirms the device belongs to that specific user, rather than only checking that it exists somewhere in the list.

### Task 8: Handle a mismatched device with `elif`

```python
approved_users = ["elarson", "bmoreno", "sgilmore", "eraab", "gesparza"]
approved_devices = ["8rp2k75", "hl0s5o1", "4n482ts", "a307vir", "3rcv4w6"]
username = "sgilmore"
device_id = "4n482tP"

ind = approved_users.index(username)

if username in approved_users and device_id == approved_devices[ind]:
    print("The user", username, "is approved to access the system.")
    print(device_id, "is the assigned device for", username)
elif username in approved_users and device_id != approved_devices[ind]:
    print("The user", username, "is approved to access the system, but", device_id, "is not their assigned device.")
```

Output: `The user sgilmore is approved to access the system, but 4n482tP is not their assigned device.`

### Task 9: Complete the algorithm as a function

```python
approved_users = ["elarson", "bmoreno", "sgilmore", "eraab", "gesparza"]
approved_devices = ["8rp2k75", "hl0s5o1", "4n482ts", "a307vir", "3rcv4w6"]

def login(username, device_id):
    if username in approved_users:
        print("The user", username, "is approved to access the system.")
        ind = approved_users.index(username)
        if device_id == approved_devices[ind]:
            print(device_id, "is the assigned device for", username)
        else:
            print(device_id, "is not their assigned device.")
    else:
        print("The username", username, "is not approved to access the system.")

login("sgilmore", "4n482tP")
```

Output:
```
The user sgilmore is approved to access the system.
4n482tP is not their assigned device.
```

The outer conditional checks whether the user is approved; the nested inner conditional then checks whether the device matches.

## Key takeaways

- `.append()` and `.remove()` add and remove list elements.
- `.index()` returns the position of an element, which can link two synchronised lists.
- The `and` operator lets a single condition verify both username and device.
- Nested conditionals inside a function combine several checks into one reusable login algorithm.
