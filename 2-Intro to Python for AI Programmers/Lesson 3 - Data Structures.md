# 1. Introduction
## In this lesson
- Types of Data Structures
    - Lists
    - Tuples
    - Sets
    - Dictionaries
    - Compound Data Structures
- Operators
    - Membership
    - Identity
- Built-In Functions and Methods

## What are Data Structures?
- are containers or collections of data
- group and order data together in different ways

## Why do we need Data Structures?
Let's now consider that you are an investment fund manager, and you want to print out the stocks (or holdings) you own in an index fund (e.g., [Vanguard Institutional Index Fund](https://www.marketwatch.com/investing/fund/vinix/holdings)). An index fund includes stocks (also called holdings) for a large number of companies. Turns out Vanguard Institutional Index Fund has [506 holdings](https://investor.vanguard.com/mutual-funds/profile/VINIX)!

Printing the tickets for all 506 holdings using individual strings would require 506 strings. Not ideal! Because we'd need to remember the name of each string to print it.

You also have to think about how to group the 506 strings under the same index fund. Not convenient at all!

This is where the beauty of data structures comes into play! You can use a list.
<br><br><br>



# 2. Lists and Membership Operators
## List
- one of the data structures in Python
- **mutable**, **ordered** sequences of elements

- to create a list:
```python
months = ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December']
```

- can contain any mix and match of the data types:
```python
list_of_random_things = [1, 3.4, 'a string', True]
```

- are ordered containers, zero base indexing (use a starting index of 0)
```python
print(months[0])
# January

print(months[1])
# February

print(months[7])
# August
```

- to pull the last element:
```python
print(months[-1])
# December
```
- this won't work:
```python
print(list_of_random_things[len(list_of_random_things)])
# IndexError: list index out of range
```
- you can do the following:
```python
print(list_of_random_things[len(list_of_random_things) - 1])
# True
```

### Slice and Dice with Lists
- to pull more than one value from a list at a time
- the lower index is inclusive and the upper index is exclusive
- you get a list back
```python
months = ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December']

q3 = months[6:9]
print(q3)
# ['July', 'August', 'September']

first_half = months[:6]
print(first_half)
# ['January', 'February', 'March', 'April', 'May', 'June']

second_half = months[6:]
print(second_half)
# ['July', 'August', 'September', 'October', 'November', 'December']
```

#### Lists and Strings
- the type of indexing of lists works exactly the same on strings (where the returned value will be a string)
greeting = "Hello there"
```python
print(len(months))
# 12
print(len(greeting))
# 11
```
```python
print(greeting[6:9])
# 'the'
print(months[6:9])
# ['July', 'August', 'September']
```

## Membership Operators
- return a bool
- whether an element exists within a list or if one string is a substring of another

| keyword | operation |
|:---:|:---|
| ```ìn```| evaluates if object on left side **is included** in object on right side |
| ```not in```| evaluates if object on left side is **not included** in object on right side |

```python
greeting = "Hello there"
print('her' in greeting)
# True
print('her' not in greeting)
# False

print('Sunday' in months)
# False
print('Sunday' not in months)
# True
```

## using Lists in the Index Fund Example
Let's return to our index fund example we discussed earlier. Since index funds have ticker symbols, for example, VINIX for the [Vanguard Institutional Index Fund](https://www.marketwatch.com/investing/fund/vinix/holdings), you can use that as the name for the list. Then we can add the ticker symbols for all the holdings into that list. Let's populate the list with the top holdings listed for Vanguard Institutional Index Fund.
```python
VINIX = ['C', 'MA', 'BA', 'PG', 'CSCO', 'VZ', 'PFE', 'HD', 'INTC', 'T', 'V', 'UNH', 'WFC', 'CVX', 'BAC', 'JNJ', 'GOOGL', 'GOOG', 'BRK.B', 'XOM', 'JPM', 'FB', 'AMZN', 'MSFT', 'AAPL']
```

- to print tickers
```python
print(VINIX[0])
# C
print(VINIX[1])
# MA
```

- to see if a particular stock is in the index fund VINIX or not
```python
print('GE' in VINIX)
# False
print('GOOGL'in VINIX)
# True
```
<br><br><br>



# 3. Mutability and Order
## Mutability
- whether an object can change its values after it has been created
- lists can be modified, are mutable
- strings are immutable
```python
months = ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December']

months[3] = 'Friday'
print(months)
# ['January', 'February', 'March', 'Friday', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December']
```

## Order
- whether thee order of elements in an object matters (and whether this can be used to access elements)
- lists and strings are ordered
<br>

- in a data structure, it's useful to understand:
- how you index
- mutability
- ordenation
<br><br><br>



# 4. Quiz: Lists and Membership Operators
## Question 1 of 3
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-4-1.png" alt="q1"/>

## Question 2 of 3
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-4-2.png" alt="q2"/>

## Question 3 of 3
Suppose we have the following two expressions, sentence1 and sentence2:
```python
sentence1 = "I wish to register a complaint."
sentence2 = ["I", "wish", "to", "register", "a", "complaint", "."]
```
Match the Python code below with the value of the modified sentence1 or sentence2. If the code results in an error, match it with “Error”.
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-4-3.png" alt="q3"/>
<br><br><br>



# 5. Solution: Lists and Membership Operators
## Question 1 of 3
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/solution-2-3-5.png" alt="solution-2-3-5"/>
<br><br><br>



# 6. List Methods
```python
name = 'Jim'
student = name
name = 'Tim'

print(name)
print(student)

# Tim
# Jim
```

```python
scores = ["B", "C", "A", "D", "B", "A"]
grades = scores
print("scores: " + str(scores))
print("grades: " + str(grades))

# scores: ["B", "C", "A", "D", "B", "A"]
# grades: ["B", "C", "A", "D", "B", "A"]
```

```python
scores = ["B", "C", "A", "D", "B", "A"]
grades = scores

scores[3] = "B"

print("scores: " + str(scores))
print("grades: " + str(grades))

# scores: ["B", "C", "A", "B", "B", "A"]
# grades: ["B", "C", "A", "B", "B", "A"]
```

| | |
|:---:|:---|
| `len()`| returns the number of elements in the list |
| `max()` | returns the greatest element of the list |
| `min()` | returns the smallest element in a list |
| `sorted()` | returns a copy of a list in order from smallest to largest - the original list remains unchanged |

### obs: max()
the max() function is defined in terms of the greater than comparison operator (>)
#### in a list of numbers:
```python
batch_sizes = [15, 6, 89, 34, 65, 35]
print(max(batch_sizes))
# 89
```
#### in a list of strings:
```python
python_varieties = ['Burmese Python', 'African Rock Python', 'Ball Python', 'Reticulated Python', 'Angolan Python']
print(max(python_varieties))
# Reticulated Python
```

### obs: sorted()
```python
sizes = [15, 6, 89, 34, 65, 35]
print(sorted(sizes))
# [6, 15, 34, 35, 65, 89]
```

```python
sizes = [15, 6, 89, 34, 65, 35]
print(sorted(sizes, reverse=True))
# [89, 65, 35, 34, 15, 6]
```


## `join`
string method that takes a list of strings as an argument, and returns a string consisting of the list elements joined by a separator string
```python
nautical_directions = "\n".join(["fore", "aft", "starboard", "port"])
print(nautical_directions)
# fore
# aft
# starboard
# port
```

```python
names = ["Garcia", "O'Kelly", "Davis"]
print("-".join(names))
# García-O'Kelly-Davis
```

It is important to remember to separate each of the items in the list you are joining with a comma (,). Forgetting to do so will not trigger an error, but will also give you unexpected results


## `append`
adds an element to the end of a list
```python
letters =  ['a', 'b', 'c', 'd']
letters.append('z')
print(letters)
# ['a', 'b', 'c', 'd', 'z']
```
<br><br><br>



# 7. Quiz: List Methods
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-7-1.png" alt="q1"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-7-2.png" alt="q2"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-7-3.png" alt="q3"/>
<br><br><br>



# 8. Check for Understanding: Lists
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-8-1.png" alt="q1"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-8-1a.png" alt="q1a"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-8-2.png" alt="q2"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-8-3.png" alt="q3"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-8-4.png" alt="q4"/>
<br><br><br>



# 9. Tuples
- data type for **immutable** (can't add and remove items or sort them in place), **ordered** sequences of elements
- often used to store related pieces of information
```python
Angkor = (13.4125, 103.866667)
print(type(AngkorWat))
print("Angkor Wat is at latitude: {}".format(AngkorWat[0]))
print("Angkor Wat is at longitude: {}".format(AngkorWat[1]))

# <class 'tuple'>
# Angkor Wat is at latitude: 13.4125
# Angkor Wat is at longitude: 103.866667
```
- can also be used to assign multiple variables in a compact way
- the parentheses are optional when defining tuples
```python
dimensions = 52, 40, 100
length, width, height = dimensions  # tuple unpacking
print("The dimensions are {}x{}x{}".format(length, width, height))

# The dimensions are 52x40x100
```
or 
```python
length, width, height = 52, 40, 100
print("The dimensions are {}x{}x{}".format(length, width, height))
```
<br><br><br>



# 10. Quiz: Tuples
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-10-1.png" alt="q1"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-10-2.png" alt="q2"/>
<br><br><br>



# 11. Sets
- data type for **mutable**, **unorded** collections of unique elements
- one application of a set is to quickly remove duplicates from a list
```python
numbers = [1, 2, 6, 3, 1, 1, 6]
unique_nums = set(numbers)
print(unique_nums)

# {1, 2, 3, 6}
```
<br><br><br>



# 12. Quiz: Sets
<br><br><br>



# 13. 
<br><br><br>



# 14. Quiz: 
<br><br><br>



# 15. Solution: