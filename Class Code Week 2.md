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

Good programming practice is to give variables meaningful names
```python
base = 10
height = 5

area = (base * height)/2

print("Area:", area)
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

Let's further enhance our example by getting the input of wage, hours and weeks from the user instead of hardcoding them.

```python
wage = input("Enter the wage rate: ")
hours = input("Enter number of hours worked: ")
weeks = input("Enter number of weeks worked: ")

salary = wage * hours * weeks
print('Salary:', salary)

```

The above program might behave unexpectedly and instead of showing us the Salary, it shows us a message like below:
```python
Traceback (most recent call last):
  File "Path\to\your\Python\file\Week_1.py", line 5, in <module>
    salary = wage * hours * weeks
             ~~~~~^~~~~~~
TypeError: can't multiply sequence by non-int of type 'str'
```
This is Python's way of giving you errors. It actually means that Python was not able to perform the operation. It gives you the line number of the error, e.g., `line 5` and the type of error, e.g., `TypeError: can't multiply sequence by non-int of type 'str'`.

The error is telling us that Python cannot perform arithematic operation on str (strings). The problem here is that `input()` function returns a string instead of a numeric value and obviously we cannot perform mathematical operations on strings; they have to be numeric values. So, what do we do? No problem, we just convert strings into numeric values. We can fix the above program but updating it as below:
```python
wage = input("Enter the wage rate: ")
hours = input("Enter number of hours worked: ")
weeks = input("Enter number of weeks worked: ")

wage = int(wage)
hours = int(hours)
weeks = int(weeks)

salary = wage * hours * weeks
print('Salary:', salary)
```
In the above code, `wage = int(wage)` means that we take the current value of wage, convert it into integer (numeric) and store it back in `wage`. Sames goes with hours and weeks as well. Since, wage, hours and weeks are now numeric, we can perform arithematic operation and then print.

You might have noticed an addition in the `print()` function. Instead of getting 1 input (argument), it is now getting 2 inputs (arguments), `'Salary'` and `salary` separate by `,`. This is Python's way of showing two outputs on the console using the same `print()` function.

### `input()` function
The `input()` function in Python is used to get user input. When you call input(), it pauses the program and waits for the user to type something and press Enter. The input is then returned as a string.

The above program can be further simplified by getting the input from the user and converting it into numeric value on the same line.
```python
wage = int(input("Enter the wage rate: ")) # user input and numeric conversion on the same line
hours = int(input("Enter number of hours worked: "))
weeks = int(input("Enter number of weeks worked: "))

salary = wage * hours * weeks
print('Salary:', salary)
```

You might have noticed `# user input and numeric conversion on the same line` in the above code. This is called a comment which is there to provide information about the line of code and would not have any impact on the program or its output.
