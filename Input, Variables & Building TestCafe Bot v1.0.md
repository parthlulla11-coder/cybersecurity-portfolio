# Python Basics — Input, Variables & Building TestCafe Bot v1.1

## 1. Introduction

In this lesson, I learned how to use the **`input()` function** to make a Python program interact with the user.

I used these concepts to build a simple **TestCafe ordering bot — v1.1**.

The bot can:

1. Welcome the customer.
2. Ask for their name.
3. Display the menu.
4. Ask for their order.
5. Ask if they want something else.
6. Confirm their order.

---

## 2. The `print()` Function

The `print()` function is used to display information in the console.

```python
print("Hi welcome to TestCafe!\n")
```

Output:

```text
Hi welcome to TestCafe!
```

The `\n` creates a **new line**.

---

## 3. The `input()` Function

The `input()` function allows the program to receive information from the user.

```python
name = input("What's your name?\n")
```

Here, several things are happening:

* `input()` asks the user for information.
* `"What's your name?\n"` is the message displayed to the user.
* The user's response is stored inside the variable `name`.

For example, if the user enters:

```text
Parth
```

Python stores that value in:

```python
name = "Parth"
```

By default, `input()` returns the user's response as a **string**.

---

## 4. Using a Variable

Once we store information inside a variable, we can use that variable later.

```python
print("hello " + name + " Thank you so much for choosing TestCafe!\n")
```

If the user entered:

```text
Parth
```

The output would be:

```text
hello Parth Thank you so much for choosing TestCafe!
```

The program is using the value stored inside `name`.

---

## 5. Creating a Menu Variable

We can also store information such as a menu inside a variable.

```python
menu = "Tea, coffee, coldrink, Beer, chicken"
```

Now the variable `menu` contains the entire menu.

We can display it using:

```python
print(menu)
```

---

## 6. Using Multiple Variables

We can combine multiple variables and strings inside `print()`.

```python
print(name + ", what would you like to have from our menu today?, Here's our Menu!\n\n" + menu)
```

If `name` contains `"Parth"` and `menu` contains the menu items, Python combines everything and displays it.

---

## 7. Taking the Customer's Order

We can use another `input()` to ask the customer for their order.

```python
Order = input()
```

The user's response is stored inside the variable `Order`.

For example:

```text
Tea
```

Python stores:

```python
Order = "Tea"
```

We can then use the variable later:

```python
print("Got It! " + name + " Is there anything you would like to have along with " + Order + "?")
```

---

## 8. Creating Another Input Variable

The customer can provide another order.

```python
Second_order = input()
```

The response is stored in `Second_order`.

The underscore (`_`) is commonly used in Python variable names instead of spaces.

For example:

```python
Second_order = "Chicken"
```

A variable cannot contain a space like this:

```python
Second order = "Chicken"  # Incorrect
```

Instead, we use:

```python
second_order = "Chicken"
```

---

## 9. Confirming the Order

Finally, we can use all the variables to confirm the customer's order.

```python
print("Perfect! " + name + " I'll have the " + Order + " And " + Second_order + " ready for you in a moment!\n")
```

For example, if:

```text
name = Parth
Order = Tea
Second_order = Chicken
```

The program could display:

```text
Perfect! Parth I'll have the Tea And Chicken ready for you in a moment!
```

---

# Complete TestCafe Bot v1.1

```python
print("Hi welcome to TestCafe!\n")

name = input("What's your name?\n")

print("hello " + name + " Thank you so much for choosing TestCafe!\n")

menu = "Tea, coffee, coldrink, Beer, chicken"

print(name + ", what would you like to have from our menu today?, Here's our Menu!\n\n" + menu)

Order = input()

print("Got It! " + name + " Is there anything you would like to have along with " + Order + "?")

print(menu)

Second_order = input()

print("Perfect! " + name + " I'll have the " + Order + " And " + Second_order + " ready for you in a moment!\n")
```

## What I Learned

In this lesson, I learned about:

* `input()`
* `print()`
* Variables
* Storing user input inside variables
* Using variables inside `print()`
* Combining strings with `+`
* Using `_` in variable names
* Building a simple interactive Python program

I used these concepts to create my **TestCafe Bot v1.0**.

Created our first bot with this concepts v1.0.
bot v.1.1 Coming soon. 
