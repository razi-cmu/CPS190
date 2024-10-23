# Week 7: Lists and Dictionaries

## Lists Basics
A list is a mutable container, meaning the size of the list can grow or shrink and elements within the list can change. `print()` method can print the list on the console.

```python
fruits = ['Apple', 'Banana', 'Grapes', 'Orange']

print(fruits)
```
Below will be the output of the above program:
```
['Apple', 'Banana', 'Grapes', 'Orange']
```

Lists can contain different types of items. Lists can stores lists inside them.
```python

fruits = ['Apple', 'Banana', 'Grapes', 'Orange', [True, 3.14]]

print(fruits)
```
Below will be the output of the above program:
```
['Apple', 'Banana', 'Grapes', 'Orange', [True, 3.14]]
```
List items can be accessed through indexing, very similar to Strings (which are actually lists of characters)
```python
fruits = ['Apple', 'Banana', 'Grapes', 'Orange', [True, 3.14]]

print(fruits[0])
```
Below will be the output of the above program:
```
Apple
```
Items within lists of lists can be accessed by multi indexing as below:
```python
fruits = ['Apple', 'Banana', 'Grapes', 'Orange', [True, 3.14]]

print(fruits[4][1])
```
Below will be the output of the above program:
```
3.14
```
## List Methods
A list method can perform a useful operation on a list such as adding or removing elements, sorting, reversing, etc.

### Append / Extend
`append` method adds an element to the end of the list.
```python
fruits = ['Apple', 'Banana', 'Grapes', 'Orange']

fruits.append('Melon')

print(fruits)
```
Below will be the output of the above program:
```
['Apple', 'Banana', 'Grapes', 'Orange', 'Melon']
```
`extend` method helps in adding a list of items to the end of the current list.
```python
fruits = ['Apple', 'Banana', 'Grapes', 'Orange']

fruits.extend(['Melon', 'Strawberry'])

print(fruits)
```
Below will be the output of the above program:
```
['Apple', 'Banana', 'Grapes', 'Orange', 'Melon', 'Strawberry']
```

### Remove / Pop
`remove` method removes a specific element from the list:
```python
fruits = ['Apple', 'Banana', 'Grapes', 'Orange']

fruits.remove('Banana')

print(fruits)
```
Below will be the output of the above program:
```
['Apple', 'Grapes', 'Orange']
```
`pop` removes the last element from the list or an element at a specific index:
```python
fruits = ['Apple', 'Banana', 'Grapes', 'Orange']

fruits.pop(2) # removes Grapes
fruits.pop()  # removes Orange

print(fruits)
```
Below will be the output of the above program:
```
['Apple', 'Banana']
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
Below will be the output of the above program:
```
THIS IS A MULTI LINE STRING.
THIS IS THE SECOND LINE.
THIS IS THE THIRD LINE.
this is a multi line string.
this is the second line.
this is the third line.
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
Below will be the output of the above program:
```
This is a multi line string.
This is the second line.
```

## String Formatting
F-string allows you to format selected parts of a string. Let's make a use of F-String to identify if a given string is a palindrome or not e.g., reads same as backwards?

```python
def is_palindrome(text):
    return text == text[::-1]

text = 'madam'

print(f"{text} is a Palindrome" if is_palindrome(text) else f"{text} is not a Palindrome")
```
Below will be the output of the above program:
```
madam is a Palindrome
```
## Joining Strings
The `join()` string method performs the inverse operation of split() by joining a list of strings together to create a single string.

```python
words = ["Python", "is", "a", "powerful", "programming", "language"]

sentence = " " .join(words)

print(sentence)
```
Below will be the output of the above program:
```
Python is a powerful programming language
```
