# Week 1: Programming with Python

## The `print()` function:
The `print()` function is a handy way of displaying an output. Mostly, the `print()` function displays the output on the console. The `print()` function takes an input which is normally called as an argument. This argument can be a string (collection of characters), an integer (numeric value), a boolean (true/false) or variables (more about variables later in this course).

* Printing a string using the `print()` function:
    ```python
    print("Hello World")
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
