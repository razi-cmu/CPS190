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

## Multiple Distinct if statements
Sometimes the programmer has multiple if statements in sequence. Each if statement is independent and more than one branch can execute. The program below is expected to output `F` matching the last `if` condition criterion.
```python
marks = 55

if marks >= 90:
    print("A")

if marks >= 80:
    print("B")

if marks >= 70:
    print("C")

if marks >= 60:
    print("D")

if marks < 60:
    print("F")
```

## If-elseif-else Branches
The program above would start acting strange as soon as we change `marks = 95`. The output will display all the grades except `F`. This is happening because each if statement is independent and they are checked against `marks = 95`. This behavior can be changed by packing all the if statement into one block making sure that only 1 if statement is executed at a time. if `marks = 95`, only first if condition should run and rest of them should be skipped. This can be achieved using if-elseif-else structure.
```python
marks = 95

if marks >= 90:
    print("A")

elif marks >= 80:
    print("B")

elif marks >= 70:
    print("C")

elif marks >= 60:
    print("D")

elif marks < 60:
    print("F")

```
Please note that elseif in Python is written as `elif`.

## Nested if-else Statements
A branch's statements can include any valid statements, including another if-else statement, which are known as nested if-else statements. The program below checks for even numbers and whether they are greater or less than 10 using nested if-else statements
```python
number = 16

if number % 2 == 0:
    if number < 10:
        print("Number is even and less than 10")
    else:
        print("Number is even and greater than 10")
else:
    print("odd")

```

## Conditional Expressions
A conditional expression has three operands and thus is sometimes referred to as a ternary operation. They are concised form of a regular if-else statement
```python
number = 17

result = "Even" if number % 2 == 0 else "Odd"

print(result)

```
