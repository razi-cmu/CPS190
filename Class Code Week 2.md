# Week 2: Variables, Expressions and Types

## Variables:
Variable is a container that holds a value, e.g., numeric, characters, and etc.
```python
number = 10

print(number)
```
Variables hold the value till a new value is assigned.

```python
number = 10

print("Original Value")
print(number)

number = 7
print("Modified Value")
print(number)
```
    
Above can be simplified into two print statements
```python
number = 10

print("Original Value:", number)

number = 7
print("Modified Value:", number)
```
## Types in Python
Python support different data types that can accomodate characters, numbers and floating point values.

### String
A string is a sequence of characters that represents textual data like a person's name, a location, or a message to the user. A string can also be stored in a variable

```python
first_name = 'Steve'
last_name = 'Jobs'

print(first_name, last_name)
```

`input()` function can help in getting an input string from the user.

```python
first_name = input('Enter first name: ')
last_name = input('Enter last name: ')

print(first_name, last_name)
```

A `+` operator in strings help in concatenating (joining) the strings:
```python
first_name = input('Enter first name: ')
last_name = input('Enter last name: ')

name = first_name + " " + last_name

print(name)
```

### Integer
An integer is a whole number that can be positive, negative, or zero, representing discrete values like counts or indexes.

```python
base = 10
height = 5

area = (base * height)/2

print("Area:", area)
```
