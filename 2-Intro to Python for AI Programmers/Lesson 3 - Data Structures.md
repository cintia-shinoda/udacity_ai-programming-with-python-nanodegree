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

- supports `in` operator:
```python
print(2 in unique_nums)
# True
```

- to add elements to sets using `add` method:
```python
unique_nums.add(8)
```

- to remove elements: `pop` method: a random element is removed
```python

```

```python
fruit = {"apple", "banana", "orange", "grapefruit"}  # define a set

print("watermelon" in fruit)  # check for element
# False

fruit.add("watermelon")  # add an element
print(fruit)
# {'grapefruit', 'orange', 'watermelon', 'banana', 'apple'}

print(fruit.pop()) # remove a random element
print(fuit)
# grapefruit
# {'orange', 'watermelon', 'banana', 'apple'}
```

- other operations: include those of mathematical sets:
  - union
  - intersection
  - difference
<br><br><br>



# 12. Quiz: Sets
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-12-1.png" alt="q1"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-12-2.png" alt="q2"/>
<br><br><br>



# 13. Dictionaries and Identity Operators
## Dictionaries
- data type for **mutable** objects that store mappings of unique keys to values
- pair key-value
- dictionaries are mutable but their keys need to be any immutable type (strings, integers, or tuples)
- it's not necessary for every key in a dictionary to have the same type

- to  look up at values: `dict_name[key]`
```python
elements = {'hydrogen': 1, 'helium': 2, 'carbon': 6}
print(elements['carbon'])
# 6
```

- to insert new values into the dictionary:
```python
elements['lithium'] = 3
print(elements)
# {'hydrogen': 1, 'helium': 2, 'carbon': 6, 'lithium': 3}
```

- to verify whether a key is in the dictionary:
```python
print('mithril' in elements)
# False
```

- `get` method:
```python
print(elements.get('dilithium'))
# None
```
  - get method is better than square bracket look-ups, because this can cause errors and crash your program:
  ```python
  print(elements['dilithium'])
  # KeyError: 'dilithium'
  ```

## Identity Operators

| keyword  | operation |
|:---:|:---|
| `is` | evaluates if both sides have the same identity |
| `is not` | evaluates if both sides have *different* identities |

- `is` operator: check if a key return None and check if a key doesn't return None with  `is not` operator
```python
n = elements.get("dilithium")
print(n is None)
print(n is not None)
# True
# False
```
<br><br><br>



# 14. Quiz: Dictionaries and Identity Operators
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-14-1.png" alt="q1"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-14-2.png" alt="q2"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-14-3.png" alt="q3"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-14-4.png" alt="q4"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-14-5.png" alt="q5"/>
  
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-14-5a.png" alt="q5a"/>
<br><br><br>



# 15. Solution: Dictionaries and Identity Operators
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/solution-2-3-14-1.png" alt="solution1"/>

```python
population = {'Shanghai': 17.8, 'Istanbul': 13.3, 'Karachi': 13.0, 'Mumbai': 12.5}
```



# 16. Quiz: More with Dictionaries
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-16-1.png" alt="q1"/>
<br><br><br>



# 17. When to Use Dictionaries?
- you also want to print a few more details for each holding. For e.g., what is your rate of return on each of the holdings?
A dictionary will work well here as there is a key: value association. In other words, there is a linkage between each holding and the information
```python
VINIX =  {'C': 0.74, 'MA': 0.78, 'BA': 0.79, 'PG': 0.85, 'CSCO': 0.88, 'VZ': 0.9, 'PFE': 0.92, 'HD': 0.97, 'INTC': 1.0, 'T': 1.01, 'V': 1.02, 'UNH': 1.02, 'WFC': 1.05, 'CVX': 1.05, 'BAC': 1.15, 'JNJ': 1.41, 'GOOGL': 1.46, 'GOOG': 1.47, 'BRK.B': 1.5, 'XOM': 1.52, 'JPM': 1.53, 'FB': 2.02, 'AMZN': 2.96, 'MSFT': 3.28, 'AAPL': 3.94}
```

You can add even other details, such as rate of return YTD. For that we can add the details into the value associated with the key, i.e., the ticker symbol for the holding.
Like this:
```python
VINIX = {'C': [0.74, -6.51],  'MA': [0.78, 34.77],  'BA': [0.79, 17.01],  'PG': [0.85, -8.81],  'CSCO': [0.88, 18.56],  'VZ': [0.9, 2.16],  'PFE': [0.92, 13.96],  'HD': [0.97, 3.2],  'INTC': [1.0, 2.61],  'T': [1.01, -15.19],  'V': [1.02, 24.0],  'UNH': [1.02, 19.32],  'WFC': [1.05, -3.59],  'CVX': [1.05, -5.77],  'BAC': [1.15, 4.27],  'JNJ': [1.41, -5.58],  'GOOGL': [1.46, 17.84],  'GOOG': [1.47, 17.03],  'BRK.B': [1.5, 4.54],  'XOM': [1.52, -6.87],  'JPM': [1.53, 7.66],  'FB': [2.02, 0.91], 'AMZN': [2.96, 62.75], 'MSFT': [3.28, 26.61], 'AAPL': [3.94, 26.01]}
```
<br><br><br>



# 18. Check for Understanding: Data Structures
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-18-1.png" alt="q1"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/solution-2-3-18-1.png" alt="solution1"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-18-2.png" alt="q2"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/solution-2-3-18-2.png" alt="solution2"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-18-3.png" alt="q3"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/solution-2-3-18-3.png" alt="solution3"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-18-4.png" alt="q4"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/solution-2-3-18-4.png" alt="solution4"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-18-5.png" alt="q5"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-18-5a.png" alt="q5a"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/solution-2-3-18-5.png" alt="solution5"/>
<br><br><br>



# 19. Compound Data Structures
- containers inside other containers
```python
elements = {"hydrogen": {"number": 1,
                         "weight": 1.00794,
                         "symbol": "H"},
              "helium": {"number": 2,
                         "weight": 4.002602,
                         "symbol": "He"}}
print(elements['helium'])
print(elements.get('unobtainium', 'There\'s no such element!'))

# {"number": 2, "symbol": "He", "weight": 4.002602}
# There's no such element!
```

```python
print(elements['helium']['weight'])
# 4.002602
```

- to add a new key to the elements dictionary:
```python
oxygen = {"number":8,"weight":15.999,"symbol":"O"}  # create a new oxygen dictionary 
elements["oxygen"] = oxygen  # assign 'oxygen' as a key to the elements dictionary
print('elements = ', elements)

# elements =  {"hydrogen": {"number": 1, "weight": 1.00794, "symbol": 'H'},
#             "helium": {"number": 2, "weight": 4.002602, "symbol": "He"}, 
#             "oxygen": {"number": 8, "weight": 15.999, "symbol": "O"}}
```
<br><br><br>



# 20. Quiz: Compound Data Structures
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-20-1.png" alt="quiz1"/>

```python
elements = {'hydrogen': {'number': 1, 'weight': 1.00794, 'symbol': 'H', 'is_noble_gas': False},
            'helium': {'number': 2, 'weight': 4.002602, 'symbol': 'He', 'is_noble_gas': True}}

# todo: Add an 'is_noble_gas' entry to the hydrogen and helium dictionaries
# hint: helium is a noble gas, hydrogen isn't

print(elements['hydrogen']['is_noble_gas'])
print(elements['helium']['is_noble_gas'])
```

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/solution-2-3-20-1.png" alt="solution1"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-20-2.png" alt="quiz2"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/solution-2-3-20-2.png" alt="solution2"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-20-3.png" alt="quiz3"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/solution-2-3-20-3.png" alt="solution3"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-3-20-4.png" alt="quiz4"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/solution-2-3-20-4.png" alt="solution4"/>
<br><br><br>



# 21. Solution: Compound Data Structures
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/solution-2-3-21.png" alt="solution21"/>
  <br><br><br>



# 22. Practice Questions
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/solution-2-3-22-1.png" alt="quiz1"/>

```python
verse = "if you can keep your head when all about you are losing theirs and blaming it on you   if you can trust yourself when all men doubt you     but make allowance for their doubting too   if you can wait and not be tired by waiting      or being lied about  don’t deal in lies   or being hated  don’t give way to hating      and yet don’t look too good  nor talk too wise"
print(verse, '\n')

# split verse into list of words
verse_list = verse.split()
print(verse_list, '\n')

# convert list to a data structure that stores unique elements
verse_set = set(verse_list)
print(verse_set, '\n')

# print the number of unique words
num_unique = len(verse_set)
print(num_unique, '\n')
  ```

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/solution-2-3-22-2.png" alt="quiz2"/>

```python
verse_dict =  {'if': 3, 'you': 6, 'can': 3, 'keep': 1, 'your': 1, 'head': 1, 'when': 2, 'all': 2, 'about': 2, 'are': 1, 'losing': 1, 'theirs': 1, 'and': 3, 'blaming': 1, 'it': 1, 'on': 1, 'trust': 1, 'yourself': 1, 'men': 1, 'doubt': 1, 'but': 1, 'make': 1, 'allowance': 1, 'for': 1, 'their': 1, 'doubting': 1, 'too': 3, 'wait': 1, 'not': 1, 'be': 1, 'tired': 1, 'by': 1, 'waiting': 1, 'or': 2, 'being': 2, 'lied': 1, 'don\'t': 3, 'deal': 1, 'in': 1, 'lies': 1, 'hated': 1, 'give': 1, 'way': 1, 'to': 1, 'hating': 1, 'yet': 1, 'look': 1, 'good': 1, 'nor': 1, 'talk': 1, 'wise': 1}
print(verse_dict, '\n')

# find number of unique keys in the dictionary
num_keys = len(verse_dict)
print(num_keys)

# find whether 'breathe' is a key in the dictionary
contains_breathe = 'breathe' in verse_dict
print(contains_breathe)

# create and sort a list of the dictionary's keys
sorted_keys = sorted(verse_dict.keys())

# get the first element in the sorted list of keys
print(sorted_keys[0])

# find the element with the highest value in the list of keys
print(sorted_keys[-1]) 
```

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/solution-2-3-22-3.png" alt="quiz3"/>
<br><br><br>



# 23. Solution: Practice Questions
## Solution: Count Unique Words
```python
verse = "if you can keep your head when all about you are losing theirs and blaming it on you   if you can trust yourself when all men doubt you     but make allowance for their doubting too   if you can wait and not be tired by waiting      or being lied about  don’t deal in lies   or being hated  don’t give way to hating      and yet don’t look too good  nor talk too wise"
print(verse, "\n")

# split verse into list of words
verse_list = verse.split()
print(verse_list, '\n')
  # ['if', 'you', 'can', 'keep', 'your', 'head', 'when', 'all', 'about', 'you', 'are', 'losing', 'theirs', 'and', 'blaming', 'it', 'on', 'you', 'if', 'you', 'can', 'trust', 'yourself', 'when', 'all', 'men', 'doubt', 'you', 'but', 'make', 'allowance', 'for', 'their', 'doubting', 'too', 'if', 'you', 'can', 'wait', 'and', 'not', 'be', 'tired', 'by', 'waiting', 'or', 'being', 'lied', 'about', 'don’t', 'deal', 'in', 'lies', 'or', 'being', 'hated', 'don’t', 'give', 'way', 'to', 'hating', 'and', 'yet', 'don’t', 'look', 'too', 'good', 'nor', 'talk', 'too', 'wise'] 

# convert list to set to get unique words
verse_set = set(verse_list)
print(verse_set, '\n')
  # {'or', 'when', 'hating', 'make', 'all', 'head', 'waiting', 'losing', 'don’t', 'to', 'look', 'about', 'yourself', 'by', 'wise', 'doubting', 'trust', 'deal', 'allowance', 'being', 'too', 'wait', 'in', 'nor', 'for', 'theirs', 'and', 'if', 'on', 'lied', 'are', 'your', 'but', 'give', 'yet', 'lies', 'good', 'men', 'tired', 'doubt', 'hated', 'blaming', 'can', 'be', 'keep', 'their', 'not', 'it', 'talk', 'way', 'you'}

# print the number of unique words
num_unique = len(verse_set)
print(num_unique)
  # 51
```

## Solution: Verse Dictionary
```python
verse_dict =  {'if': 3, 'you': 6, 'can': 3, 'keep': 1, 'your': 1, 'head': 1, 'when': 2, 'all': 2, 'about': 2, 'are': 1, 'losing': 1, 'theirs': 1, 'and': 3, 'blaming': 1, 'it': 1, 'on': 1, 'trust': 1, 'yourself': 1, 'men': 1, 'doubt': 1, 'but': 1, 'make': 1, 'allowance': 1, 'for': 1, 'their': 1, 'doubting': 1, 'too': 3, 'wait': 1, 'not': 1, 'be': 1, 'tired': 1, 'by': 1, 'waiting': 1, 'or': 2, 'being': 2, 'lied': 1, 'don\'t': 3, 'deal': 1, 'in': 1, 'lies': 1, 'hated': 1, 'give': 1, 'way': 1, 'to': 1, 'hating': 1, 'yet': 1, 'look': 1, 'good': 1, 'nor': 1, 'talk': 1, 'wise': 1}
print(verse_dict, '\n')

# find number of unique keys in the dictionary
num_keys = len(verse_dict)
print(num_keys)
  # 51

# find whether 'breathe' is a key in the dictionary
contains_breathe = "breathe" in verse_dict
print(contains_breathe)
  # False

# create and sort a list of the dictionary's keys
sorted_keys = sorted(verse_dict.keys())

# get the first element in the sorted list of keys
print(sorted_keys[0])
  # about

# find the element with the highest value in the list of keys
print(sorted_keys[-1]) 
  # yourself
```
<br><br><br>



# 24. Conclusion
## Congratulations on completing this lesson on Data Structures!

| Data Structure | Ordered | Mutable | Constructor | Example |
|:---:|:---:|:---:|:---|:---|
| List | Yes | Yes | `[ ]` or `list()` | `[5.7, 4, 'yes', 5.7]` |
| Tuple | Yes | No | `( )` or `tuple()` | `(5.7, 4, 'yes', 5.7)` |
| Set | No | Yes | `{ }`* or `set()` | `{5.7, 4, 'yes'}` |
| Dictionary | No | No** | `{ }` or `dict()` | `{'Jun': 75, 'Jul':89}` 

* You can use curly braces to define a set like this: `{1, 2, 3}`. However, if you leave the curly braces empty like this: `{}` Python will instead create an empty dictionary. So to create an empty set, use `set()`.
** A dictionary itself is mutable, but each of its individual keys must be immutable.