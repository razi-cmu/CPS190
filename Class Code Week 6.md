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
## String Slicing
Multiple consecutive characters can be read using slice notation. The code below will print first two lines of the string using String Slicing.

```python
text = """This is a multi line string.
This is the second line.
This is the third line."""

print('First Line:', text[0:28])
print('Second Line:', text[29:53])
```

## String Functions

String objects have many useful methods to do things like replacing characters, converting to lowercase, capitalizing the first character, etc. The program below will convert all the lines of text into upper and lower case.

```python
text = """This is a multi line string.
This is the second line.
This is the third line."""

print(text.upper())
print(text.lower())

```

Let's get a bit more creative now. How about we write a function that takes in the text along with number of lines and prints us only that many lines.

```python
def get_lines(text, number):
    
    lines = text.splitlines()
    
    for line in lines[:number]:
        print(line)


text = """This is a multi line string.
This is the second line.
This is the third line."""

get_lines(text, 2)


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
