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

<br><br><br>



# 3. Mutability and Order
<br><br><br>



# 4. Quiz: Lists and Membership Operators
<br><br><br>



# 5. Solution: Lists and Membership Operators
<br><br><br>