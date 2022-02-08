# 1. Introduction
topics covered:
- **Data Types:** Integers, Floats, Booleans, Strings
- **Operators:** Arithmetic, Assignment, Comparison, Logical
- **Built-In Functions**, **Type Conversion**
- **Whitespace** and **Style Guidelines**
- `print()` : built-in function that displays input values *as text* in the output
<br><br><br>



# 2. Arithmetic Operators

| Symbol | Operation |
|:---:|:---:|
| + | addition |
| - | subtraction |
| * | multiplication |
| / | division |
| % | mod (the remainder after dividing) |
| ** | exponentiation |
| // | the rounded result of a division to the nearest integer |

- The usual order of mathematical operations holds in Python
- [Bitwise Operators](https://wiki.python.org/moin/BitwiseOperators) are special operators in Python
<br><br><br>



# 3. Quiz: Arithmetic Operators
## Question 1 of 3
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-3-1.png" alt="q1"/>

  ## Question 2 of 3
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-3-2.png" alt="q2"/>

## Question 3 of 3
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-3-3.png" alt="q3"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-3-3a.png" alt="q3-comment"/>
<br><br><br>



# 4. Solution: Arithmetic Operators
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/solution-2-2-4.png" alt="solutions"/>
<br><br><br>



# 5. Variables and Assignment Operators
- whatever term is on the left side, is now a name for whatever value is on the right side. 
- once a value has been assigned to a variable name, you can access the value from the variable name
`mv_population = 74728`
- to assign multiple varibles at once:
```
x = 3
y = 4
z = 5
```

or

```x, y, z = 3, 4, 5```

- variables names should be descriptive of the values they hold
    - only use ordinary letters, numbers and underscores
    - need to start with a letter or underscore
    - can't have spaces
    - can't use reserved words or built-in identifiers

#### keywords in Python

||||||
|:---:|:---:|:---:|:---:|:---:|
| False | class | finally | is | return|
| None | continue | for | lambda | try |
| True | def | from | nonlocal | while |
| and | del | global | not | with |
| as | elif | if | or | yield |
| assert | else | import | pass | |
| break | except | in | raise | |

- use all lowercase and underscores to separate words (snakecase)
<br><br>

## Assignment Operators

| symbol | example | equivalent |
|:---:|:---:|:---:|
| `=` | `x = 2` | `x = 2` |
| `+=` | `x += 2` | `x = x + 2` |
| `-=` | `x -= 2` | `x = x - 2` |
| `*=` | `x *= 2` | `x = x * 2` |

[Practice](https://www.programiz.com/python-programming/operators)
<br><br><br>



# 6. Quiz: Variables and Assignment Operators
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-6-1.png" alt="q1"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-6-2a.png" alt="q2a"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-6-2b.png" alt="q2b"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-6-3.png" alt="q3"/>
<br><br><br>



# 7. Solution: Variables and Assignment Operators
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/solution-2-2-7-1.png" alt="solution-1"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-7-2.png" alt="solution-2"/>
<br><br><br>



# 8. Integers and Floats
- data types used for numeric values
    - **int:** for integer values
    - **float:** for decimal ou floating point values
- to convert:
``` python
x = int(4.7)  # x = 4
y = float(4)  # y = 4.0 
```

- to check the type:
``` python
print(type(x))  # int
print(type(y))  # float
```

- [the float or approximation, for 0.1 is slightly more than 0.1](https://docs.python.org/3/tutorial/floatingpoint.html), when added several of them together there will be a difference between the mathematically correct answer and the one that Python creates
``` python
print(.1 + .1 + .1 == 3)
# False
```

## Python Best Practices
- Although how you format the code doesn’t affect how it runs, following standard style guidelines makes code easier to read and consistent among different developers on a team.

[PEP8 Guidelines](https://www.python.org/dev/peps/pep-0008/)

- limit each line of code to 80 characters

[Why is 80 characters the "standard" limit for code width?](https://softwareengineering.stackexchange.com/questions/148677/why-is-80-characters-the-standard-limit-for-code-width)
<br><br><br>



# 9. Quiz: Integers and Floats
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-9-1.png" alt="q1"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-9-2.png" alt="q2"/>

- Traceback means "What was the programming doing when it broke"! This part is usually less helpful than the very last line of your error.

- 2 types of errors to look out for:
    - **exceptions:** is a problem that occurs when the code is running
    - **syntax:** is a problem detected when Python checks the code before it runs it
- for more about[Errors and Exceptions](https://docs.python.org/3/tutorial/errors.htmlhttps://docs.python.org/3/tutorial/errors.html)
<br><br><br>



# 10. Booleans, Comparison Operators, and Logical Operators
- **bool:**
    - data type
    - can be `True` or `False` or encoded as 1 or 0, respectively

#### Comparison Operators
| Symbol | Operation |
|:---:|:---:|
| `<` | less than |
| `>` | greater than |
| `<=` | less than or equal to |
| `>=` | greater than or equal to |
| `==` | equal to |
| `!=` | not equal to

#### Logical Operators
| Symbol | Operation |
|:---:|:---:|
| `and` | evaluates if all provideed statements are True |
| `or` | evaluates if at least of many statements is True |
| `not` | flips the bool value |


- more about [George Boole](https://www.irishtimes.com/news/science/how-george-boole-s-zeroes-and-ones-changed-the-world-1.2014673)
<br><br><br>



# 11. Quiz: Booleans, Comparison Operators, and Logical Operators
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-11-1.png" alt="q1"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-11-2.png" alt="q2"/>
<br><br><br>



# 12. Solution: Booleans, Comparison Operators, and Logical Operators
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/solution-2-2-12.png" alt="solution1"/>
<br><br><br>



# 13. Strings
- **string (```str```):** data type for immutable ordered sequences of characters (e.g. letters, numbers, spaces, and symbols)
- to create strings: 
```python
print("hello")  # double quotes
print('hello')  # single quotes
```

- to assign a string to a variable
```python
welcome_message = "Hello, welcome to Udacity!"
print(welcome_message)
```

- when we want quotation marks in our strings:
  - place the string in single quotes
  ```python
  pet_halibut = 'why should I be tarred with the epithet "loony" merely because I have a pet halibut?'
  ```
  - use a backslash to escape quotes
    ```python
    salesman = '"I think you\'re an encyclopaedia salesman"'
    ```
- operations with strings:
  - to put strings together(concatenate) ```+```  
  ```python
  first_word = "Hello"
  second_word = "There"
  print(first_word + second_word)
  # HelloThere

  print(first_word + " " + second_word)
  # Hello There
  ```
  - to repeat strings ```*```
  ```python
  word = "Hello"
  print(word * 5)
  # HelloHelloHelloHelloHello
  ```

- ```len()``` : built-in function that returns the length (in strings is the number of characters in the string) of an object - will always be a integer
  ```python
  udacity_length = len("Udacity")
  print(udacity_length)
  # 7

  print(len("ababa") / len("ab"))
  # 2.5
  ```

- you can index into strings
```python
first_word = "Hello"

first_word[0]
# H
first_word[1]
# e
```
<br><br><br>



# 14. Quiz: Strings
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-14-1.png" alt="quiz1"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-14-2.png" alt="quiz2"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-14-3.png" alt="quiz3"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-14-3a.png" alt="comment"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-14-4.png" alt="quiz4"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-14-5.png" alt="quiz5"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-14-5a.png" alt="comment"/>
<br><br><br>



# 15. Solution: Strings
## Solution: Fiz the Quote
  ```python 
  ford_quote = 'Whether you think you can, or you think you can\'t--you\'re right.'

  ford_quote = "Whether you think you can, or you think you can't--you're right."
  ```

  <p align="center">
    <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/solution-2-2-15.png" alt="solution15"/>
<br><br><br>



# 16. Type and Type Conversion
- 4 data types so far:
  - `int`
  - `float`
  - `bool`
  - `string`

- check the data type:
  ```python
  print(type(633))
  # int

  print(type(633.0))
  # float

  print(type("633"))
  # str

  print(type(True))
  # bool
  ```

- `int` from a `float`:
  ```python
  count = int(4.0)
  print(count)
  print(type(count))
  # 4
  # class 'int'
  ```

- 
  ```python
  house_number = 13
  street_name = "The Crescent"
  town_name = "Belmont"
  print(type(house_number))
  # class 'int'

  address = str(house_number) + " " + street_name + ", " + town_name
  print(address)
  # 13 The Crescent, Belmont
<br><br><br>



# 17. Quiz: Type and Type Conversion
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-17-1.png" alt="quiz1"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-17-2.png" alt="quiz2"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-17-3.png" alt="quiz3"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-17-4.png" alt="quiz4"/>
  
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-2-17-5.png" alt="quiz5"/>
<br><br><br>



# 18. Solution: Type and Type Conversion
## Solution: Total Sales
  ```python
  weekly_sales = int(mon_sales) + int(tues_sales) + int(wed_sales) + int(thurs_sales) + int(fri_sales)
  weekly_sales = str(weekly_sales)  #convert the type back!!
  print("This week's total sales: " + weekly_sales)
  ```
<br><br><br>



# 19. String Methods

<br><br><br>



# 20. Quiz: String Methods
<br><br><br>