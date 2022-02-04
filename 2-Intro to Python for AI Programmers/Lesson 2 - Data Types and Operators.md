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
    ### keywords in Python
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
## Assignment Operators

| symbol | example | equivalent |
|:---:|:---:|:---:|
| `=` | `x = 2` | `x = 2` |
| `+=` | `x += 2` | `x = x + 2` |
| `-=` | `x -= 2` | `x = x - 2` |
| `*=` | `x *= 2` | `x = x * 2` |

[Practice](https://www.programiz.com/python-programming/operators)

<br><br><br>