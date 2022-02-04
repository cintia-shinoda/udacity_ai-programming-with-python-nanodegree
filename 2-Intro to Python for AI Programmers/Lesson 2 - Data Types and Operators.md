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

    <table>
        <tr>
            <td>False</td>
            <td>class</td>
            <td>finally</td>
            <td>is</td>
            <td>return</td>
        </tr>
        <tr>
            <td>None</td>
            <td>continue</td>
            <td>for</td>
            <td>lambda</td>
            <td>try</td>
        </tr>
        <tr>
            <td>True</td>
            <td>def</td>
            <td>from</td>
            <td>nonlocal</td>
            <td>while</td>
        </tr>
        <tr>
            <td>and</td>
            <td>del</td>
            <td>global</td>
            <td>not</td>
            <td>with</td>
        </tr>
        <tr>
            <td>as</td>
            <td>elif</td>
            <td>if</td>
            <td>or</td>
            <td>yield</td>
        </tr>
           <tr>
            <td>assert</td>
            <td>else</td>
            <td>import</td>
            <td>pass</td>
            <td></td>
        </tr>
       <tr>
            <td>break</td>
            <td>except</td>
            <td>in</td>
            <td>raise</td>
            <td></td>
        </tr>
    </table>

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

<br><br><br>



# 12. Solution: Booleans, Comparison Operators, and Logical Operators
<br><br><br>



# 13. Strings
<br><br><br>



# 14. Quiz: Strings
<br><br><br>



# 15. Solution: Strings
<br><br><br>