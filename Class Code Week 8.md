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
fruits = ['Apple', 'Banana', 'Grapes', 'Orange', [True, 3.14]]

print(fruits[0])
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
    print('Cannot divided by zero.')

print('Program exited successfully')

```
Below will be the output of the above program:
```
Cannot divided by zero.
Program exited successfully
```
## Multiple Exception Handler
A list method can perform a useful operation on a list such as adding or removing elements, sorting, reversing, etc.

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



## Iterating over the List

Looping through a sequence such as a list is so common that Python supports a construct called a for loop, specifically for iteration purposes. Let's write a function in Python that removes duplicates from a give list. We do this by iterating through the given list, item by item.

```python
def remove_duplicates(fruits):
    new_fruits = []

    for fruit in fruits:
        if fruit not in new_fruits:
            new_fruits.append(fruit)
    
    return new_fruits

fruits = ['Melon','Apple', 'Banana', 'Grapes', 'Orange', 'Apple', 'Grapes']

print(remove_duplicates(fruits))
```
Below will be the output of the above program:
```
['Melon', 'Apple', 'Banana', 'Grapes', 'Orange']
```

## List Comprehension
The Python language provides a convenient construct, known as list comprehension, that iterates over a list, modifies each element, and returns a new list of the modified elements. 

Let's rewrite the above program using List comprehension:

```python
def remove_duplicates(fruits):
    new_fruits = []

    [new_fruits.append(fruit) for fruit in fruits if fruit not in new_fruits]
    
    return new_fruits

fruits = ['Melon','Apple', 'Banana', 'Grapes', 'Orange', 'Apple', 'Grapes']

print(remove_duplicates(fruits))
```
Below will be the output of the above program:
```
['Melon', 'Apple', 'Banana', 'Grapes', 'Orange']
```
## Dictionary Basics
Dictionaries contain references to objects as key-value pairs — each key in the dictionary is associated with a value, much like each word in an English language dictionary is associated with a definition.

```python
electronics = {
    'name': 'Laptop',
    'price': 500,
    'quantity': 3
}

print(electronics)
```
Below will be the output of the above program:
```
{'name': 'Laptop', 'price': 500, 'quantity': 3}
```

Dictionaries in Python can hold Lists as their items as well:
```python
electronics = {
    'name': ['Laptop', 'Keyboard', 'Mouse'],
    'price': [500, 100, 30],
    'quantity': [3, 2, 4]
}

print(electronics)
```
Below will be the output of the above program:
```
{'name': ['Laptop', 'Keyboard', 'Mouse'], 'price': [500, 100, 30], 'quantity': [3, 2, 4]}
```

## Iterating over the Dictionary
The above output is not very easy to understand. We can make it easier to understanding by iterating through each item along with their corresponding prices and quantities:
```python
def display(electronics):
    for name, price, quantity in zip(electronics['name'], electronics['price'], electronics['quantity']):
        print(f'There are {quantity} {name}s each with a price tag of {price}')


electronics = {
    'name': ['Laptop', 'Keyboard', 'Mouse'],
    'price': [500, 100, 30],
    'quantity': [3, 2, 4]
}


display(electronics)
```
Below will be the output of the above program:
```
There are 3 Laptops each with a price tag of 500
There are 2 Keyboards each with a price tag of 100
There are 4 Mouses each with a price tag of 30
```
