# Week 5: Strings

## Strings Basics
Strings are a sequence type, having characters ordered by index from left to right. Below is a multiline string stored in a variable in Python.

```python
text = """This is a multi line string.
This is the second line.
This is the third line."""

print(text)
```
Since Strings in Python are array based, we can access the characters of string using indices, e.g., str[0] to get the first character of the array.

```python
text = """This is a multi line string.
This is the second line.
This is the third line."""

print('First character:', text[0])
print('Last character:', text[-1])
print('No. of Characters:', len(text))
```
## String Slicing
Multiple consecutive characters can be read using slice notation. The code below will print first two lines of the string using String Slicing.

```python
text = """This is a multi line string.
This is the second line.
This is the third line."""

print('First Line:', text[0:28])
print('Second Line:', text[29:53])
```

## String Functions

String objects have many useful methods to do things like replacing characters, converting to lowercase, capitalizing the first character, etc. The program below will convert all the lines of text into upper and lower case.

```python
text = """This is a multi line string.
This is the second line.
This is the third line."""

print(text.upper())
print(text.lower())

```

Let's get a bit more creative now. How about we write a function that takes in the text along with number of lines and prints us only that many lines.

```python
def get_lines(text, number):
    
    lines = text.splitlines()
    
    for line in lines[:number]:
        print(line)


text = """This is a multi line string.
This is the second line.
This is the third line."""

get_lines(text, 2)

```

## String Formatting
F-string allows you to format selected parts of a string. Let's make a use of F-String to identify if a given string is a palindrome or not e.g., reads same as backwards?

```python
def is_palindrome(text):
    return text == text[::-1]

text = 'madam'

print(f"{text} is a Palindrome" if is_palindrome(text) else f"{text} is not a Palindrome")
```

## Joining Strings
The `join()` string method performs the inverse operation of split() by joining a list of strings together to create a single string.

```python
words = ["Python", "is", "a", "powerful", "programming", "language"]

sentence = " " .join(words)

print(sentence)
```
