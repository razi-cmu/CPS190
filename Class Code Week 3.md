# Week 3: Branching

## Branch Basics
In a program, a branch is a sequence of statements only executed under a certain condition.
```python
marks = 65

if marks > 60:
    print("pass")
```

## if-else Branching
The above program would only display pass if marks are greater than 65, however, it would display anything if marks are less than 65. In order to tackle both pass and fail conditions, if-else branching can be used.
```python
marks = 65

if marks > 60:
    print("pass")
else:
    print("fail")
```

## Multiple Dstinct if statements
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
