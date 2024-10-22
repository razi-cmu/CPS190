# Week 5: Strings

## Strings Basics
Strings are a sequence type, having characters ordered by index from left to right. Below is a multiline string stored in a variable in Python.

```python
text = """This is a multi line string.
This is the second line.
This is the third line."""

print(text)
```
Since Strings in Python are array based, we can access the characters of string using indices, e.g., str[0] to get the first character of the array.

```python
text = """This is a multi line string.
This is the second line.
This is the third line."""

print('First character:', text[0])
print('Last character:', text[-1])
print('No. of Characters:', len(text))
```
## Return Statement
The function return statement is used to exit from a function and go back to the function caller and return the specified value or data item to the caller. In some cases, you might not want function to print but to simply return the result of the calculation.

The function below will calculate the sum of all the numbers from 1 to 5 and then return the result, e.g., `15` instead of printing it. Once the result is returned, we might want to perform some operation on it, e.g., printing.
```python
def calculate_sum():
    sum = 0
    for i in range(1, 6):
        sum = sum + i

    return sum

print(calculate_sum())
```

## Functions with Arguments

Arguments are the values passed inside the parenthesis of the function. These values provide extra information to the function which that make these functions more flexible.


```python
def calculate_sum(start, end):
    sum = 0
    for i in range(start, end):
        sum = sum + i

    return sum

print(calculate_sum(1, 6))
```

## Keyword Arguments
Python provides for keyword arguments that allow arguments to map to parameters by name, instead of implicitly by position in the argument list. This makes function calls more readable and easier to understand.

```python
def calculate_sum(start, end):
    sum = 0
    for i in range(start, end):
        sum = sum + i

    return sum

print(calculate_sum(start=1, end=6))
```

## Default Parameter Values
A function can have a default parameter value for one or more parameters, meaning that a function call can optionally omit an argument, and the default parameter value will be substituted for the corresponding omitted argument.

Let's update our program so that `end` is always `6`.
```python
def calculate_sum(start, end=6):
    sum = 0
    for i in range(start, end):
        sum = sum + i

    return sum

print(calculate_sum(start=1))
```
