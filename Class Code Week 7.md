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

### Sort / Reverse
`sorted` method helps in sorting the list in ascending order:
```python
fruits = ['Melon','Apple', 'Banana', 'Grapes', 'Orange']

fruits.sort()

print(fruits)
```
Below will be the output of the above program:
```
['Apple', 'Banana', 'Grapes', 'Melon', 'Orange']
```
`reverse` method reverses the list:
```python
fruits = ['Melon','Apple', 'Banana', 'Grapes', 'Orange']

fruits.reverse()

print(fruits)
```
Below will be the output of the above program:
```
['Orange', 'Grapes', 'Banana', 'Apple', 'Melon']
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
