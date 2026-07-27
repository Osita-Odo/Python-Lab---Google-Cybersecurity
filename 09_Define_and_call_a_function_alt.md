# Define and Call a Function (Alternate Version)

This lab covers the same material as *Define and Call a Function*, with one difference in how the string is accumulated in Task 6. Refer to that README for Tasks 1–5 and Task 7; the note below highlights the variation.

## Scenario

A security analyst defines and calls an `alert()` function, then builds a `list_to_string()` function that converts a list of usernames into a single string.

## Variation in Task 6: printing inside the loop

In this version, a space is used as the separator and `print()` is placed inside the loop, so the string is displayed at each stage as it grows.

```python
def list_to_string():
    username_list = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab",
                     "gesparza", "alevitsk", "wjaffrey"]
    sum_variable = ""
    for i in username_list:
        sum_variable = sum_variable + i + " "
        print(sum_variable)

list_to_string()
```

Output:
```
elarson
elarson bmoreno
elarson bmoreno tshah
elarson bmoreno tshah sgilmore
elarson bmoreno tshah sgilmore eraab
elarson bmoreno tshah sgilmore eraab gesparza
elarson bmoreno tshah sgilmore eraab gesparza alevitsk
elarson bmoreno tshah sgilmore eraab gesparza alevitsk wjaffrey
```

Because `print()` runs on every iteration, the growing string is shown at each step. Placing `print()` outside the loop instead would display only the final combined string.

## Key takeaway

The position of `print()`, inside or outside a loop, determines whether output appears once at the end or on every iteration. This is a useful distinction for tracing how a value is built up.
