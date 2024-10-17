# Week 4: Loops

## Loop Basics
If we want to write a program that displays numbers from 1 to 10, we can use `print()` in a traditional form as below:
```python
print(1)
print(2)
print(3)
print(4)
print(5)
print(6)
print(7)
print(8)
print(9)
print(10)
```
The above will be a cumbersome job if we decided to print numbers from 1 to 1000.

## While Loop
A loop is a program construct that repeatedly executes the loop's statements (known as the loop body) while the loop's expression is true. A while loop is a construct that repeatedly executes an indented block of code (known as the loop body) as long as the loop's expression is True.

We can rewrite the above code using `while` loop which would be much more efficient.
```python
i = 1
while (i <= 10):
    print(i)
    i = i + 1
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
