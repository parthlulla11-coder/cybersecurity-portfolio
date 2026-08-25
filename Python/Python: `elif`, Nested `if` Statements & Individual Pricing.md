# Python: `elif`, Nested `if` Statements & Individual Pricing

## What I Learned

In this lesson, I learned how to use **`elif` statements**, **nested `if` statements**, and how to assign **individual prices** to different items in my Test Cafe bot.

---

## 1. `elif` Statements

`elif` is used when I want to check multiple conditions.

Instead of writing separate `if` statements, I can use `elif` to check another condition when the previous condition is `False`.

```python
if order == "Chicken":
    price = 350
elif order == "Beer":
    price = 200
elif order == "Wine":
    price = 250
```

Python checks the conditions from top to bottom and runs the first condition that matches.

---

## 2. Nested `if` Statements

A **nested `if` statement** is an `if` statement placed inside another `if` statement.

This allows the program to make another decision after an initial condition has been met.

```python
if order == "Chicken":
    price = 350

    if quantity > 1:
        print("Multiple orders selected")
```

The inner `if` is dependent on the outer `if` being executed.

This is useful when a program needs to make more detailed decisions.

---

## 3. Individual Prices

I also learned how to give each item its own price instead of using one fixed price.

```python
if order == "Chicken":
    price = 350
elif order == "Beer":
    price = 200
elif order == "Wine":
    price = 250
```

This makes the Test Cafe bot more realistic because different items can have different prices.

---

## 4. Combining What I Learned

The main goal of this exercise was to start making the Test Cafe bot more advanced by combining:

* `if`
* `elif`
* `else`
* Nested `if`
* Variables
* Individual item prices

The bot can now identify the selected item and assign the appropriate price.

---

## Key Takeaways

* `elif` allows multiple conditions to be checked.
* `elif` is useful when there are several possible choices.
* A nested `if` is an `if` statement inside another `if` statement.
* Different items can be assigned different prices using variables.
* Conditional logic makes the Test Cafe bot more dynamic and realistic.

## Progress

**Previously learned:**

* Variables
* Strings
* `input()`
* Basic `if` statements

**New in this lesson:**

* `elif`
* Nested `if` statements
* Individual pricing
* Applying these concepts to the Test Cafe bot
