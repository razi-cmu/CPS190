# Week 5: Functions

## Function Basics
Program redundancy can be reduced by creating a grouping of predefined statements for repeated operations, known as a function. A function definition consists of the function's name and a block of statements. The function below calculates the sum of numbers from 1 to 5.
```python
def calculate_sum():
    sum = 0
    for i in range(1, 6):
        sum = sum + i

    print(sum)

calculate_sum()
```

## Return Statement
The function return statement is used to exit from a function and go back to the function caller and return the specified value or data item to the caller. In some cases, you might not want function to print but to simply return the result of the calculation.

The function below will calculate the sum of all the numbers from 1 to 5 and then return the result, e.g., 15 instead of printing it. Once the result is returned, we might want to perform some operation on it, e.g., printing.
```python
def calculate_sum():
    sum = 0
    for i in range(1, 6):
        sum = sum + i

    return sum

print(calculate_sum())
```

Let's now print all the even numbers from 1 and 20 using `while` loop.
```python
i = 1
while (i <= 20):
    if (i % 2 == 0):
        print(i)
    i = i + 1

```

## For Loop
A for loop statement loops over each element in a container one at a time, assigning a variable with the next element that can then be used in the loop body. Let's print even numbers from 1 and 20 using a `for` loop.
```python
for i in range(1, 21):
    if (i%2 == 0):
        print(i)
```
A `for` loop helps in iterating through strings or any other collections (list, dictionary etc. coming up)
```python
word = "Python"

for character in word:
    print(character)
```

## Nested Loops
A nested loop is a loop that appears as part of the body of another loop. The nested loops are commonly referred to as the outer loop and inner loop.

Let's write a program that creates a grid of `*`. We are planning to create a 5x5 grid of `*`. The output should be something like below:
```
*****
*****
*****
*****
*****
```
The above can be achieved easily with 5 `print()` statements. However, imagine modifying it to a grid of 100x100. With loops, number of print statements would not change and a slight change in how many rows and columns we need can provide us a grid of any size.

```python
rows = 0
while (rows < 5):
    columns = 0
    while (columns < 5):
        print('*', end='')
        columns+=1
    print()
    rows+=1
```

## Break Statement
A break statement in a loop causes the loop to exit immediately.

Let's create a program that keeps generating random numbers till it generates `5`. As soon as the generated number is `5`, the program breaks the loop and exits the program.
```python
import random

while (True):
    number = int(random.random() * 10)
    print('Number generated: ', number)
    if (number == 5):
        break
```

We are using a built-in library `random` to generate random numbers using `random()` function.

## Continue Statement
A continue statement in a loop causes an immediate jump to the while or for loop header statement.

Let's create a program that reads all the characters of a word and skip an `e` in it.
```python
word = 'Hello'

for ch in word:
    if (ch == 'e'):
        continue
    print(ch, end='')

```
