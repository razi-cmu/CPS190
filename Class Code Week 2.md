# Week 2: Variables, Expressions and Types

## Variables:
Variable is a container that holds a value, e.g., numeric, characters, and etc.
```python
number = 10

print(number)
```
    Strings can be printing using the `print()` function with "" or ''. Below code will also produce the same output on the console, e.g., `Hello World`

    ```python
    print('Hello World')
    ```
    
* Printing numeric values using the `print()` function:
    ```python
    print(1)
    ```

   `print()` function has the ability to print floating point values as well. 

    ```python
    print(1.58)
    ```

* Printing boolean values using the `print()` function:
    ```python
    print(True)
    ```

   Similarly, `False` can be printing by passing `False` to the `print` function. Please note that except character collections (String) no other output used a "" or '' for printing.

    ```python
    print(1.58)
    ```

* Printing expressions using the `print()` function:
    ```python
    print(2+2)
    ```

    The `print` function can also solve and print mathematical expressions. It is normally not recommended to perform printing of complex mathematical expression directly in the `print` function to avoid readability issues. For example an arithematic expression $`2^3 - \frac{8}{5} + 2^{-1}`$ can be written and evaluated in Python using the following code:
  ```python
  print(2**3 - 8/5 + 2**-1)
  ```

  The above might not be too easy to read. It is a good idea to store them in variables and then use/print them:
  ```python
  z = 2**3 - 8/5 + 2**-1
  print(z)
  ```

  The above expression can be furthe simplified by dividing it into different components as below:
  ```python
  a = 2**3
  b = 8/5
  c = 2**-1

  z = a - b + c
  print(z)
  ```
  `a`, `b`, `c` and `z` in the above Python code are called `Variables`. We'll talk about variables in more detail in coming weeks.

## Working with real problems in Python
We have seen the working of a `print()` function with strings, numerics and expressions. We can can combine them all to solve a real world problem. Let's write code to solve a real world problem:

### Problem 
Write a Python program that calculates the salary of an employee provided wage rate, hour and weeks. Print the calculated salary on the console in `Salary: 1234` format.

```python
wage = 20
hours = 40
weeks = 52
salary = wage * hours * weeks

print('Salary:', salary)
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
