# TestCafe Bot v1.2 — Run Process

## Overview

Version **1.2** builds on the previous versions of the TestCafe Bot.

### Previous versions

* **v1.0** — Basic customer interaction and two-item ordering.
* **v1.1** — Added quantity, price, and bill calculations.

The new features in v1.2 include:

* Banned customer check.
* Menu display.
* First order and quantity.
* Option to add a second item.
* Second item quantity.
* Calculation of two separate bills.
* Calculation of the final total.

> **Note:** The current code does not yet include the "greater than 10" restriction mentioned in the update log. That feature should only be listed once it is added to the code.

---

# Step-by-Step Run Process

## 1. Display the Welcome Message

```python
print("Hi welcome to TestCafe!\n")
```

The program starts by displaying a welcome message.

The `\n` creates a new line after the message.

---

## 2. Ask for the Customer's Name

```python
name = input("What's your name?\n")
```

The program asks the customer to enter their name.

The input is stored in the `name` variable.

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

## 3. Check Whether the Customer Is Banned

```python
if name == "ben" or name == "Ben":
```

The program checks whether the customer's name is `"ben"` or `"Ben"`.

The `or` operator allows Python to check both conditions.

If either condition is true, this code runs:

```python
print("I'm sorry " + name + ". I'm afraid you're Banned from the cafe!.")
exit()
```

The program:

1. Displays the banned message.
2. Runs `exit()`.
3. Stops the program.

This means the rest of the ordering system does not run.

---

## 4. Continue if the Customer Is Not Banned

```python
else:
    print("hello " + name + " Thank you so much for choosing Testcafe!\n")
```

If the customer's name is not `ben` or `Ben`, the condition is false.

Python then runs the `else` block and welcomes the customer.

For example:

```text
hello Parth Thank you so much for choosing Testcafe!
```

---

# 5. Create the Menu

```python
menu = "tea, coffee, coldrink, Beer, chicken"
```

The available menu items are stored in the `menu` variable.

This allows the program to display the same menu whenever it is needed.

---

## 6. Display the Menu

```python
print(name + ", what would you like to have from our menu today?, Here's our Menu!\n\n" + menu)
```

The program displays the customer's name and the available menu.

The customer can then choose their first item.

---

## 7. Store the First Order

```python
order = input()
```

The customer's first choice is stored in the `order` variable.

For example:

```text
tea
```

Python stores:

```python
order = "tea"
```

---

## 8. Set the Price

```python
price = 20
```

In the current version, every menu item has a fixed price of **₹20**.

The `price` variable is used later to calculate the bill.

---

## 9. Ask for the First Order Quantity

```python
quantity = input("Good Choice! How many " + order + "?" " would you like to have?\n")
```

The program asks the customer how many of the first item they would like.

The answer is stored in:

```python
quantity
```

Because `input()` returns a string, a response such as:

```text
3
```

is initially stored as:

```python
quantity = "3"
```

It will later be converted into an integer using `int()` for the bill calculation.

---

## 10. Ask Whether the Customer Wants a Second Item

```python
order_2 = input("Is there anything you would like to pair with your beer? " + order + "?\n")
```

The program asks the customer whether they would like to add another item.

The response is stored in the `order_2` variable.

For example:

```text
yes
```

---

# 11. Check the Customer's Response

```python
if order_2 == "yes" or order_2 == "yeah" or order_2 == "Yes" or order_2 == "YES":
```

The program checks whether the customer wants another item.

It currently accepts the following responses:

```text
yes
yeah
Yes
YES
```

If one of these conditions is true, the program starts the second-order process.

If none of these conditions are true, Python runs the `else` block.

---

# 12. Ask for the Second Order

If the customer wants another item, the program asks them to select one from the menu.

```python
order_2 = input("Noted! " + name + " What can i get you? \n " + menu)
```

The customer's second item replaces the previous `order_2` value.

For example:

```text
coffee
```

Python now stores:

```python
order_2 = "coffee"
```

---

## 13. Ask for the Second Order Quantity

```python
quantity_2 = input("How many " + order_2 + " would you like to have?\n")
```

The program asks how many of the second item the customer wants.

For example:

```text
2
```

Python initially stores:

```python
quantity_2 = "2"
```

Again, the value is a string because it came from `input()`.

---

# 14. Calculate the First Bill

```python
bill = price * int(quantity)
```

The first quantity is converted into an integer:

```python
int(quantity)
```

Python then multiplies the quantity by the price.

For example:

```text
Price: ₹20
Quantity: 3

20 × 3 = ₹60
```

The result is stored in:

```python
bill
```

---

# 15. Calculate the Second Bill

```python
bill_2 = price * int(quantity_2)
```

The same process happens for the second order.

For example:

```text
Price: ₹20
Quantity: 2

20 × 2 = ₹40
```

The result is stored in:

```python
bill_2
```

---

# 16. Calculate the Final Total

```python
total = int(bill) + int(bill_2)
```

The program adds both bills together.

For example:

```text
First bill: ₹60
Second bill: ₹40

Total: ₹100
```

The final amount is stored in the `total` variable.

---

## 17. Display Both Orders and the Final Bill

```python
print("Noted I'll have your " + order + " & " + order_2 + " ready, meanwhile here is your total bill - " + str(total) + " INR")
```

The final output includes:

* The first order.
* The second order.
* The total bill.

`str(total)` converts the final number into a string so it can be combined with the rest of the message.

Example:

```text
Noted I'll have your tea & coffee ready, meanwhile here is your total bill - 100 INR
```

---

# 18. If the Customer Does Not Want a Second Item

If the customer's response does not match any of the accepted answers:

```python
yes
yeah
Yes
YES
```

Python runs the `else` block.

First, it displays:

```python
final_order = print("Gotcha!")
```

Then it calculates the bill for only the first order:

```python
bill = price * int(quantity)
```

For example:

```text
Price: ₹20
Quantity: 3

20 × 3 = ₹60
```

Finally, the program displays the first order and its total bill:

```python
print("Noted I'll have your " + order + "Right away, total bill is " + str(bill) + "INR")
```

---

# v1.2 Program Flow

```text
Start
  ↓
Welcome Customer
  ↓
Ask for Name
  ↓
Is the name "ben" or "Ben"?
  ├── Yes → Display Banned Message → Stop Program
  │
  └── No → Welcome Customer
              ↓
          Display Menu
              ↓
          Take First Order
              ↓
          Ask for Quantity
              ↓
       Ask if Customer Wants Another Item
              ↓
        ┌─────────────┴─────────────┐
       Yes                          No
        ↓                            ↓
   Select Second Item          Calculate First Bill
        ↓                            ↓
   Ask for Quantity                 Display Bill
        ↓
   Calculate First Bill
        ↓
   Calculate Second Bill
        ↓
   Add Both Bills
        ↓
   Display Final Total
```

---

# What I Added in v1.2

Compared with **v1.1**, I added:

* A banned customer check.
* `if` and `else` statements.
* Multiple conditions using `or`.
* The `exit()` function.
* A second-order option.
* A second quantity variable.
* A second bill calculation.
* A final total that combines two bills.
* Different program paths depending on the customer's response.

---

# Concepts Used

This version combines concepts from my previous Python lessons:

### Input and Output

```python
print()
input()
```

### Variables

```python
name
menu
order
quantity
price
bill
order_2
quantity_2
bill_2
total
```

### Conditional Statements

```python
if
else
```

### Comparison

```python
==
```

### Logical Operator

```python
or
```

### Type Conversion

```python
int()
str()
```

### Arithmetic

```python
*
+
```

### Stopping the Program

```python
exit()
```

---

# Version Progress

| Version  | Main Features                                                                              |
| -------- | ------------------------------------------------------------------------------------------ |
| **v1.0** | Basic interaction and two orders                                                           |
| **v1.1** | Quantity, price, and bill calculation                                                      |
| **v1.2** | Conditional logic, banned user check, optional second order, and combined bill calculation |

## Next Improvements

As I continue learning Python, I plan to improve the bot further by adding:

* Different prices for different menu items.
* Better validation for customer input.
* A quantity limit feature.
* More flexible yes/no responses.
* Multiple menu items.
* More advanced conditional logic.
* Loops and functions.
