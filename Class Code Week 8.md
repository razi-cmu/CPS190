# Week 8: Exception Handling

## Exception Basics
An exception is an unexpected behaviour of a program that might occur did to an error in the code. The program below will crash with an error:

```python
print(x)
```
Below will be the output of the above program:
```
Traceback (most recent call last):
  File "c:\Users\iqbal1r\Documents\CPS190\Week_3.py", line 2, in <module>
    print(x)
          ^
NameError: name 'x' is not defined
```

In order to fix the above program so that it does not crash, we can use the concept of Exception Handling in Python.
```python
try:
    print(x)
except:
    print("An error occured. x is not defined")
```
Below will be the output of the above program:
```
An error occured. x is not defined
```

## Common Exception Types
There are several types of exceptions available in Python. A common one is `ZeroDivisionError` that occurs when a number is divided by zero
```python
number = 5
result = number / 0
print(result)

print('Program exited successfully')
```
Below will be the output of the above program:
```
Traceback (most recent call last):
  File "c:\Users\iqbal1r\Documents\CPS190\Week_3.py", line 2, in <module>
    result = number / 0
             ~~~~~~~^~~
ZeroDivisionError: division by zero
```
You might have noticed that `Program exited successfully` was not printed on the console as it crashed before the control can reach that print statement. This can be fixed by putting the vulnerable code in the try block.
```python
try:
    number = 5
    result = number / 0
    print(result)
except:
    print('Cannot divide by zero.')

print('Program exited successfully')

```
Below will be the output of the above program:
```
Cannot divide by zero.
Program exited successfully
```
## Multiple Exception Handlers
Multiple Exception Handlers can be introduced in a try-except. The program below demonstrates the use of two different types of handlers; one for ZeroDivisionError and the other is NameError

```python
try:
    number = 5
    result = number / 2
    print(result)

    print(x)
except ZeroDivisionError:
    print('Cannot divided by zero.')
except NameError:
    print('Variable not defined.')

print('Program exited successfully')

```
Below will be the output of the above program:
```
2.5
Variable not defined.
Program exited successfully
```

## Exceptions with Functions

If an exception is raised within a function and is not handled within that function, then the function is immediately exited. The calling function is checked for a handler, and so on up the function call hierarchy.

The program below crashes because it tries to access an index of a list which is not available. Hence, it crashes the function and then the whole program.
```python
def sum_of_elements(numbers):
    sum = 0
    for i in range(len(numbers) + 1):
        sum += numbers[i]

    return sum

numbers = [1, 2, 3, 4, 5]

print(sum_of_elements(numbers))
```
Below will be the output of the above program:
```
Traceback (most recent call last):
  File "c:\Users\iqbal1r\Documents\CPS190\Week_3.py", line 13, in <module>
    print(sum_of_elements(numbers))
          ~~~~~~~~~~~~~~~^^^^^^^^^
  File "c:\Users\iqbal1r\Documents\CPS190\Week_3.py", line 6, in sum_of_elements
    sum += numbers[i]
           ~~~~~~~^^^
IndexError: list index out of range
```

There are a couple of ways of fixing the above program. One of the ways and probably the easiest one is to handle the exception inside the function:
```python
def sum_of_elements(numbers):
    try:
        sum = 0
        for i in range(len(numbers) + 1):
            sum += numbers[i]

        return sum
    except:
        print("Index out of bound")
        return 0

numbers = [1, 2, 3, 4, 5]

print(sum_of_elements(numbers))
```

Below will be the output of the above program:
```
Index out of bound
0
```

Another way of fixing it is by handling the exception at the calling method, e.g., `print()`:
```python
def sum_of_elements(numbers):
    
    sum = 0
    for i in range(len(numbers) + 1):
        sum += numbers[i]

    return sum


numbers = [1, 2, 3, 4, 5]
try:
    print(sum_of_elements(numbers))
except:
    print('Index out of bound')

```
Below will be the output of the above program:
```
Index out of bound
```
## Finally
Python provides a keyword finally, which is always executed after the try and except blocks.

```python
try:
    result = 5/0 
    print(result)

except ZeroDivisionError:
    print("Can't divide by zero")

finally:
    print('This is always executed')

print('The program exited successfully.')
```
Below will be the output of the above program:
```
Can't divide by zero
This is always executed
The program exited successfully.
```
The above message `This is always executed` will still be executed if exception does not occur. This allows a programmer to specify clean-up actions that are always executed.
