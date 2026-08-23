# TestCafe Bot — Python Learning Progress

This is my first Python project: a simple **TestCafe ordering bot**.

I started with a basic version that could interact with a customer and take an order. After learning more Python concepts, I improved the bot in **v1.1** by adding quantity, price, and bill calculations.

---

# Version 1.0 — Basic Ordering Bot

## Overview

The first version of the TestCafe Bot focuses on the basics of making a Python program interact with a user.

The bot can:

* Display a welcome message.
* Ask for the customer's name.
* Display a menu.
* Take the customer's first order.
* Ask if they want another item.
* Take a second order.
* Confirm the order.

At this stage, the bot **does not calculate prices or quantities**.

---

## v1.0 Code

```python
print("Hi welcome to TestCafe!\n")

name = input("What's your name?\n")

print("hello " + name + " Thank you so much for choosing Testcafe!\n")

menu = "Tea, coffee, coldrink, Beer, chicken"

print(name + ", what would you like to have from our menu today?, Here's our Menu!\n\n" + menu)

Order = input()

print("Got It! " + name + " Is there anything you would like to have along with " + Order + "?")

print(menu)

Second_order = input()

print("Perfect! " + name + " I'll have the " + Order + " And " + Second_order + " ready for you in a moment!\n")
```

---

## v1.0 Run Process

### 1. Welcome Message

```python
print("Hi welcome to TestCafe!\n")
```

The `print()` function displays the welcome message.

The `\n` creates a new line.

---

### 2. Ask for the Customer's Name

```python
name = input("What's your name?\n")
```

The `input()` function asks the customer for their name.

Whatever the customer enters is stored in the `name` variable.

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

### 3. Use the Name in the Program

```python
print("hello " + name + " Thank you so much for choosing Testcafe!\n")
```

The program takes the value stored in `name` and combines it with other strings using `+`.

If the customer entered `Parth`, the program displays:

```text
hello Parth Thank you so much for choosing Testcafe!
```

---

### 4. Create the Menu

```python
menu = "Tea, coffee, coldrink, Beer, chicken"
```

The menu is stored inside the `menu` variable.

This allows the program to use the menu later.

---

### 5. Display the Menu

```python
print(name + ", what would you like to have from our menu today?, Here's our Menu!\n\n" + menu)
```

The program combines the customer's name with the menu and displays it.

---

### 6. Take the First Order

```python
Order = input()
```

The program waits for the customer to enter an item.

The response is stored in the `Order` variable.

For example:

```text
Tea
```

is stored as:

```python
Order = "Tea"
```

---

### 7. Ask for Another Item

```python
print("Got It! " + name + " Is there anything you would like to have along with " + Order + "?")
```

The program uses both the customer's name and their first order to ask whether they want something else.

---

### 8. Display the Menu Again

```python
print(menu)
```

The menu is displayed again so the customer can choose another item.

---

### 9. Take the Second Order

```python
Second_order = input()
```

The customer's second choice is stored in the `Second_order` variable.

The underscore `_` is used instead of a space because Python variable names cannot contain spaces.

---

### 10. Confirm the Order

```python
print("Perfect! " + name + " I'll have the " + Order + " And " + Second_order + " ready for you in a moment!\n")
```

The program combines the customer's name and both orders to create a final confirmation message.

---

# What I Learned in v1.0

This version helped me learn the basics of:

* `print()`
* `input()`
* Variables
* Strings
* Storing user input
* Using variables later in the program
* Combining strings using `+`
* Using `\n` for new lines
* Using `_` in variable names

---

# Version 1.1 — Adding Price & Quantity

## Overview

After completing v1.0, I learned more Python concepts and used them to make the bot more advanced.

The biggest change in **v1.1** is that the bot can now:

* Ask what the customer wants.
* Ask how many they want.
* Set a price.
* Calculate the total bill.
* Display the final amount.

This introduced two important concepts:

```python
int()
```

and

```python
str()
```

---

## v1.1 Code

```python
print("Hi welcome to TestCafe!\n")

name = input("What's your name?\n")

print("hello " + name + " Thank you so much for choosing Testcafe!\n")

menu = "tea, coffee, coldrink, Beer, chicken"

print(name + ", what would you like to have from our menu today?, Here's our Menu!\n\n" + menu)

order = input()

price = 20

quantity = input("Good Choice! How many " + order + " you like to have?\n")

bill = price * int(quantity)

print("thank you for that, the total would be " + str(bill) + "INR")
```

---

# v1.1 Run Process

### 1. Welcome and Customer Name

The first few lines work similarly to v1.0.

```python
print("Hi welcome to TestCafe!\n")

name = input("What's your name?\n")

print("hello " + name + " Thank you so much for choosing Testcafe!\n")
```

The program welcomes the customer, stores their name, and uses the name in the welcome message.

---

### 2. Create and Display the Menu

```python
menu = "tea, coffee, coldrink, Beer, chicken"

print(name + ", what would you like to have from our menu today?, Here's our Menu!\n\n" + menu)
```

The menu is stored in a variable and then displayed to the customer.

---

### 3. Store the Order

```python
order = input()
```

The customer's choice is stored in the `order` variable.

For example:

```text
tea
```

becomes:

```python
order = "tea"
```

---

### 4. Set the Price

```python
price = 20
```

In v1.1, I introduced a price variable.

For now, every item costs **₹20**.

This is a basic system that I plan to improve in future versions.

---

### 5. Ask for Quantity

```python
quantity = input("Good Choice! How many " + order + " you like to have?\n")
```

The bot now asks the customer how many of the selected item they want.

For example:

```text
Good Choice! How many tea you like to have?
3
```

The value entered by the customer is stored in `quantity`.

However, `input()` stores the value as a **string**.

So:

```python
quantity = "3"
```

not:

```python
quantity = 3
```

---

### 6. Convert the Quantity to an Integer

To perform mathematical calculations, I need to convert the quantity from a string into an integer.

I use:

```python
int(quantity)
```

For example:

```python
int("3")
```

becomes:

```python
3
```

---

### 7. Calculate the Bill

```python
bill = price * int(quantity)
```

Now Python can multiply the price by the quantity.

For example:

```text
Price = ₹20
Quantity = 3
```

Python calculates:

```text
20 × 3 = 60
```

The result is stored in:

```python
bill
```

So:

```python
bill = 60
```

---

### 8. Convert the Bill Back to a String

The final line is:

```python
print("thank you for that, the total would be " + str(bill) + "INR")
```

The `bill` is an integer, but I'm combining it with text using `+`.

I therefore use:

```python
str(bill)
```

to convert the number into a string.

For example:

```python
str(60)
```

becomes:

```python
"60"
```

The final output becomes:

```text
thank you for that, the total would be 60INR
```

---

# v1.0 vs v1.1

| Feature             | v1.0 | v1.1 |
| ------------------- | ---- | ---- |
| Welcome message     | ✅    | ✅    |
| Ask customer's name | ✅    | ✅    |
| Display menu        | ✅    | ✅    |
| Take order          | ✅    | ✅    |
| Second order        | ✅    | ❌    |
| Ask quantity        | ❌    | ✅    |
| Price               | ❌    | ✅    |
| Calculate total     | ❌    | ✅    |
| `int()`             | ❌    | ✅    |
| `str()`             | ❌    | ✅    |
| Bill                | ❌    | ✅    |

---

# What I Learned From v1.0 → v1.1

The biggest difference between these versions is that **v1.0 taught me how to make the program interact with the user**, while **v1.1 taught me how to use the user's input to perform a calculation**.

### v1.0

I learned:

* `print()`
* `input()`
* Variables
* Strings
* String concatenation
* `\n`

### v1.1

I built on those concepts and learned:

* Integers
* `int()`
* `str()`
* Arithmetic with variables
* Multiplication
* Calculating a bill
* Converting user input so Python can perform calculations

---

# Project Progress

## TestCafe Bot v1.0

**Goal:** Build a basic interactive café ordering program.

The bot could communicate with the customer and take two orders.

## TestCafe Bot v1.1

**Goal:** Make the bot more useful by introducing quantity and price calculations.

The bot can now calculate the customer's total bill.

## Future Development

As I continue learning Python, I will keep upgrading the bot.

Possible future improvements include:

* Different prices for different menu items.
* Multiple items in one order.
* Better menu organization.
* Order confirmation.
* More advanced calculations.
* Conditional statements.
* Loops.
* Functions.

This project is being developed alongside my Python learning, so each new version will reflect the new concepts I learn.
