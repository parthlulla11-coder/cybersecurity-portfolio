# Python Basics — If Statements, Else, Comparison Operators & `exit()`

## Introduction

In this lesson, I learned how to make a Python program **make decisions**.

Previously, my TestCafe Bot could take input from the user and perform calculations. Now I can make the program check information and decide what to do based on the user's input.

The main concepts I learned are:

* `if`
* `else`
* `==`
* `or`
* Comparison operators
* `exit()`

I used these concepts to add a **banned customer check** and a simple **number guessing game** to my TestCafe program.

---

# The Code

```python
print("Hi welcome to TestCafe!\n")

name = input("What's your name?\n")

if name == "ben" or name == "Ben":
    print("I'm sorry " + name + ". I'm afraid you're Banned from the cafe!.")
    exit()
else:
    print("hello " + name + " Thank you so much for choosing Testcafe!\n")

number = input("Guess the number between 1 and 10!\n")

if number == "1":
    print("Correct!")
else:
    print("Wrong number!")
```

---

# Run Process

## 1. Welcome the Customer

```python
print("Hi welcome to TestCafe!\n")
```

The program starts by displaying a welcome message.

The `\n` moves the cursor to a new line.

---

## 2. Ask for the Customer's Name

```python
name = input("What's your name?\n")
```

The program asks the user for their name.

Whatever the user enters is stored in the `name` variable.

For example:

```text
What's your name?
Parth
```

Python stores:

```python
name = "Parth"
```

---

# 3. Using an `if` Statement

```python
if name == "ben" or name == "Ben":
```

This is where the program starts making a decision.

The `if` statement checks whether a condition is **True**.

In this case, Python checks:

```text
Is name equal to "ben"?
OR
Is name equal to "Ben"?
```

If either condition is true, the code inside the `if` block runs.

---

## 4. The Banned Customer Check

```python
print("I'm sorry " + name + ". I'm afraid you're Banned from the cafe!.")
```

If the customer enters `ben` or `Ben`, the program displays the banned message.

For example:

```text
What's your name?
Ben

I'm sorry Ben. I'm afraid you're Banned from the cafe!.
```

---

# 5. The `or` Operator

```python
if name == "ben" or name == "Ben":
```

`or` allows us to check **more than one condition**.

The condition is true if **at least one** of the conditions is true.

For example:

```python
name == "ben" or name == "Ben"
```

If the user enters:

```text
ben
```

the first condition is true.

If the user enters:

```text
Ben
```

the second condition is true.

In either case, the `if` block runs.

---

# 6. The `exit()` Function

```python
exit()
```

`exit()` stops the program.

In this project, I use it after identifying a banned customer.

So if the user enters `Ben`, the program:

1. Detects the name.
2. Prints the banned message.
3. Runs `exit()`.
4. Stops running the rest of the code.

The number guessing game will therefore **not run** for the banned customer.

---

# 7. The `else` Statement

```python
else:
    print("hello " + name + " Thank you so much for choosing Testcafe!\n")
```

`else` runs when the `if` condition is **False**.

For example, if the user enters:

```text
Parth
```

this condition:

```python
name == "ben" or name == "Ben"
```

is false.

Therefore, Python runs the `else` block.

The customer receives:

```text
hello Parth Thank you so much for choosing Testcafe!
```

---

# 8. The `==` Operator

One of the most important things I learned here is the difference between:

```python
=
```

and:

```python
==
```

### `=`

A single `=` is used to **assign a value** to a variable.

For example:

```python
name = "Parth"
```

This means:

> Store `"Parth"` inside the variable `name`.

---

### `==`

A double `==` is used to **compare two values**.

For example:

```python
name == "Parth"
```

This asks Python:

> Is the value stored in `name` equal to `"Parth"`?

The result will be either:

```text
True
```

or:

```text
False
```

---

# 9. Comparison Operators

Comparison operators allow us to compare values.

The main operators I learned are:

| Operator | Meaning                  | Example  |
| -------- | ------------------------ | -------- |
| `==`     | Equal to                 | `x == 5` |
| `>`      | Greater than             | `x > 5`  |
| `<`      | Less than                | `x < 5`  |
| `>=`     | Greater than or equal to | `x >= 5` |
| `<=`     | Less than or equal to    | `x <= 5` |

These comparisons produce a Boolean result:

```text
True
```

or:

```text
False
```

---

# 10. Number Guessing Game

After the name check, the program asks the user to guess a number.

```python
number = input("Guess the number between 1 and 10!\n")
```

The user's answer is stored in the `number` variable.

For example:

```text
Guess the number between 1 and 10!
1
```

Python stores the input as:

```python
number = "1"
```

Remember that `input()` returns a string by default.

---

# 11. Checking the Number

```python
if number == "1":
    print("Correct!")
else:
    print("Wrong number!")
```

The program checks whether the user entered `"1"`.

If they did:

```text
Correct!
```

If they entered anything else:

```text
Wrong number!
```

---

# Important Observation

In this version, `"1"` is written as a string:

```python
number == "1"
```

This is because `input()` gives us a string.

If we wanted `number` to be an integer instead, we could convert it:

```python
number = int(input("Guess the number between 1 and 10!\n"))
```

Then we could compare it with the integer:

```python
if number == 1:
```

This connects directly to what I learned in **TestCafe Bot v1.1**, where I learned about `int()`.

---

# What I Learned

In this lesson, I learned how to make Python programs make decisions.

### `if`

Runs code when a condition is true.

```python
if name == "Parth":
    print("Welcome!")
```

### `else`

Runs when the `if` condition is false.

```python
else:
    print("Access denied!")
```

### `==`

Compares two values.

```python
name == "Parth"
```

### `or`

Allows multiple conditions to be checked.

```python
if name == "ben" or name == "Ben":
```

### Comparison Operators

I learned how to compare values using:

```python
==
>
<
>=
<=
```

### `exit()`

Stops the program from running.

```python
exit()
```

---

# What Changed in My Python Learning?

Previously, my programs mainly **followed instructions from top to bottom**.

With `if` and `else`, I can now make the program **choose what happens next**.

For example:

```text
User enters name
       ↓
Is the name Ben?
   ↙         ↘
 YES          NO
 ↓             ↓
Ban user     Welcome user
 ↓             ↓
Exit        Continue program
```

This is an important step because conditional statements are the foundation for making programs behave differently depending on the information they receive.

---

# Next Step

I can now start combining:

* Variables
* `input()`
* `print()`
* `int()`
* `str()`
* Arithmetic
* `if`
* `else`
* Comparison operators

This will allow me to make the **TestCafe Bot** much more advanced in future versions.
