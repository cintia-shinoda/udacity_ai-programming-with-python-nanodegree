# 1. Introduction
## Control Flow
- describes the order in which the lines of code are run
- this order is usually different then the sequence in which the lines of code appear
- execution can flow from one place in the code to another

    - conditional statements
    - boolean expressions
    - For and While loops
    - Break and Continue
    - Zip and Enumerate
    - useful built-in functions
    - list comprehensions 
<br><br><br>



# 2. Conditional Statements
## `if` Statement
- is a conditional statement that runs or skips code based on whether a condition is True or False.
```python
if phone_balance < 5:
    phone_balance += 10
    bank_balance -= 10
```
### Use Comparison Operators in Conditional Statements
`>, <, >=, <=, ==, !=


## `if`, `elif`, `else`
```python
n = 4

if n % 2 == 0:
    print("Number " + str(n) + " is even.")
else:
    print("Number " + str(n) + " is odd.")

# Number 4 is even.
```

```python
season = "spring"

if season == "spring":
    print("plant the garden!")
elif season == "summer":
    print("water the garden!")
elif season == "fall":
    print("harvest the garden!")
elif season == "winter":
    print("stay indoors!")
else:
    print("unrecognized season")

# plant the garden!
```

### Remember: `=` vs. `==`
`=` assignment operator
`==` comparison operator


## Indentation
- used to enclose blocks of code
- in Python, indents conventionally come in multiples of four spaces
- be strict about following this convention, because changing the indentation can completely change the meaning of the code

## Spaces of Tabs?
- the [Python Style Guide](https://www.python.org/dev/peps/pep-0008/#tabs-or-spaces) recommends using 4 spaces to indent, rather than using a tab
- "Python 3 disallows mixing the use of tabs and spaces for indentation."

```python
phone_balance = 8
bank_balance = 100
print(phone_balance, bank_balance)

if phone_balance < 5:
    phone_balance += 10
    bank_balance -= 10

print(phone_balance, bank_balance)
```

## Try It Out!
Use Test Run to execute the following code, which includes several examples of if statements. 
Experiment with different inputs and see what is printed out. 
Can you follow the flow of logic to figure out which code lines will get run? If you're not sure, you can insert additional print statements to help you figure out how it works.

```python
#First Example - try changing the value of phone_balance
phone_balance = 10
bank_balance = 50

if phone_balance < 10:
    phone_balance += 10
    bank_balance -= 10

print(phone_balance)
print(bank_balance)

# 10
# 50


#Second Example - try changing the value of number

number = 145
if number % 2 == 0:
    print("Number " + str(number) + " is even.")
else:
    print("Number " + str(number) + " is odd.")

# Number 145 is odd.


#Third Example - try to change the value of age
age = 35

# Here are the age limits for bus fares
free_up_to_age = 4
child_up_to_age = 18
senior_from_age = 65

# These lines determine the bus fare prices
concession_ticket = 1.25
adult_ticket = 2.50

# Here is the logic for bus fare prices
if age <= free_up_to_age:
    ticket_price = 0
elif age <= child_up_to_age:
    ticket_price = concession_ticket
elif age >= senior_from_age:
    ticket_price = concession_ticket
else:
    ticket_price = adult_ticket

message = "Somebody who is {} years old will pay ${} to ride the bus.".format(age, ticket_price)
print(message)

# Somebody who is 35 years old will pay $2.5 to ride the bus.
```
<br><br><br>



# 3. Practice: Conditional Statements
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/practice-2-4-3.png" alt="practice-2-4-3"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/practice-2-4-3a.png" alt="practice-2-4-3a"/>
<br><br><br>



# 4. Solution: Conditional Statements
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/practice-solution-2-4-3.png" alt="practice-2-4-3"/>
<br><br><br>



# 5. Quiz: Conditional Statements
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-4-5-1.png" alt="quiz-2-4-5-1"/>

<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-4-5-2.png" alt="quiz-2-4-5-2"/>
<br><br><br>



# 6. Solution: Conditional Statements
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/solution-2-4-5-1.png" alt="solution-2-4-5-1"/>

## Solution: Tax Purchase
```python
state = 'CA'
purchase_amount = 20.00    # a sample state and purchase amount

if state == 'CA':
    tax_amount = .075
    total_cost = purchase_amount*(1+tax_amount)
    result = "Since you're from {}, your total cost is {}.".format(state, total_cost)

elif state == 'MN':
    tax_amount = .095
    total_cost = purchase_amount*(1+tax_amount)
    result = "Since you're from {}, your total cost is {}.".format(state, total_cost)

elif state == 'NY':
    tax_amount = .089
    total_cost = purchase_amount*(1+tax_amount)
    result = "Since you're from {}, your total cost is {}.".format(state, total_cost)

print(result)

# Since you're from CA, your total cost is 21.5.
```
<br><br><br>



# 7. Boolean Expressions for Conditions
## Complex Boolean Expressions
```python
if 18.5 <= weight / height ** 2 < 25:
    print("BMI is considered 'normal'")

if is raining and is_sunny:
    print("Is there a rainbow?")

if (not unsubscribed) and (location == "USA" or location == "CAN"):
    print("send email")
```


## Good and Bad Examples
1. don't use `if True:` or `if False:`
```python
if True:
    print("This indent code will always get run")
```

```python
if is_cold or not is_cold:
    print("This indent code will always get run")
```
2. be careful writing expressions that use logical operators (`and`, `or`, `not`)
```python
if weather == "snow" or "rain":
    print("wear boots!")
```
3. don't evaluate the truth of a boolean variable with `== True` or `== False` : the variable itself is a boolean expression
```python
if is_cold == True:
    print("The weather is cold!")
```
instead, use like this:
```python
if is_cold:
    print("The weather is cold!")
```


## Truth Value Testing
```python
errors = 3
if errors:
    print("You have {} errors to fix!".format(errors))
else:
    print("No errors to fix!")
```
<br><br><br>



# 8. Quiz: Boolean Expressions for Conditions
<p align="center">
  <img src="https://github.com/cintia-shinoda/udacity_ai-programming-with-python-nanodegree/blob/master/images/quiz-2-4-8-1.png" alt="quiz1"/>

<br><br><br>



# 9. Solution: Boolean Expressions for Conditions
<br><br><br>



# 10. For Loops
<br><br><br>



# 11. Practice: For Loops
<br><br><br>



# 12. Solution: For Loops Practice



# 13. Quiz: For Loops
<br><br><br>



# 14. Solution: For Loops Quiz
<br><br><br>