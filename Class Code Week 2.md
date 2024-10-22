# Week 2: Variables, Expressions and Types

## Variables:
Variable is a container that holds a value, e.g., numeric, characters, and etc.
```python
number = 10

print(number)
```
Below will be the output of the above program:
```
10
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
Below will be the output of the above program:
```
Original Value
10
Modified Value
7
```

Above can be simplified into two print statements
```python
number = 10

print("Original Value:", number)

number = 7
print("Modified Value:", number)
```

Below will be the output of the above program:
```
Original Value: 10
Modified Value: 7
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
Below will be the output of the above program:
```
Steve Jobs
```
`input()` function can help in getting an input string from the user.

```python
first_name = input('Enter first name: ')
last_name = input('Enter last name: ')

print(first_name, last_name)
```
Below will be the output of the above program:
```
Enter first name: Steve
Enter last name: Jobs
Steve Jobs
```
A `+` operator in strings help in concatenating (joining) the strings:
```python
first_name = input('Enter first name: ')
last_name = input('Enter last name: ')

name = first_name + " " + last_name

print(name)
```
Below will be the output of the above program:
```
Enter first name: Steve
Enter last name: Jobs
Steve Jobs
```
### Integer
An integer is a whole number that can be positive, negative, or zero, representing discrete values like counts or indexes. The program below helps in finding the area of the Triangle.

```python
base = 10
height = 5

area = (base * height)/2

print("Area:", area)
```
Below will be the output of the above program:
```
Area: 25.0
```
### Float
A float is a number that includes a decimal point, representing real numbers with fractional parts. The program below helps in finding the area of the circle.

```python
radius = 4.2
pi = 3.14

area = pi * (radius**2)

print(area)
```
Below will be the output of the above program:
```
55.3896
```
Instead of hardcoding the value of `pi`, we can use built-in `Math` library.
```python
import math

radius = 4.2

print("Value of Pi:", math.pi)

area = math.pi * (radius**2)

print(area)
```
Below will be the output of the above program:
```
Value of Pi: 3.141592653589793
55.41769440932395
```
