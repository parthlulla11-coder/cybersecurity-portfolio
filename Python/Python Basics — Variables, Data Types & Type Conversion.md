# Python Basics — Variables, Data Types & Type Conversion

## 1. Variables

A **variable** is a name used to store a value.

```python
intro = "Hi, My name is Parth\n"
age = "31"
integer = 26
actual_age = 26.5
```

Here, we created four variables:

* `intro` stores a string.
* `age` stores a string because `"31"` is inside quotation marks.
* `integer` stores a whole number.
* `actual_age` stores a decimal number.

---

## 2. Strings

A **string (`str`)** is text surrounded by quotation marks.

```python
name = "Parth"
age = "31"
```

Even though `31` looks like a number, Python treats it as a string because it is inside `" "`.

We can check the data type using `type()`:

```python
print(type(age))
```

Output:

```text
<class 'str'>
```

### Important

Anything inside quotation marks is treated as a string.

```python
"31"    # string
"Hello" # string
```

---

## 3. Integers

An **integer (`int`)** is a whole number without a decimal point.

```python
age = 26
```

We can check its type:

```python
print(type(age))
```

Output:

```text
<class 'int'>
```

Examples of integers:

```python
10
25
100
-5
0
```

---

## 4. Floating-Point Numbers

A **float (`float`)** is a number that contains a decimal point.

```python
actual_age = 26.5
```

We can check its type:

```python
print(type(actual_age))
```

Output:

```text
<class 'float'>
```

Examples:

```python
10.5
25.75
3.14
0.5
```

---

## 5. Checking Data Types with `type()`

Python provides the `type()` function to tell us what type of data a value contains.

```python
age = "31"
integer = 26
actual_age = 26.5

print(type(age))
print(type(integer))
print(type(actual_age))
```

Output:

```text
<class 'str'>
<class 'int'>
<class 'float'>
```

This is useful when we aren't sure what type of data a variable contains.

---

## 6. Combining Strings

We can use `+` to join strings together.

```python
intro = "Hi, My name is Parth\n"
age = "31"

print(intro + age)
```

The `+` operator joins the two strings together.

Because both values are strings, Python can concatenate them.

---

## 7. Basic Arithmetic

Python can also perform mathematical calculations.

### Addition

```python
print(5 + 5)
```

Output:

```text
10
```

### Multiplication

```python
print(5 * 5)
```

Output:

```text
25
```

Python supports several arithmetic operators:

| Operator | Meaning        |
| -------- | -------------- |
| `+`      | Addition       |
| `-`      | Subtraction    |
| `*`      | Multiplication |
| `/`      | Division       |

For example:

```python
print(5 * 5 / 2 - 4 * 100)
```

Python evaluates the mathematical expression according to its operator precedence.

---

## 8. Converting Data Types

Sometimes we need to convert one data type into another.

Python provides functions such as:

```python
int()
str()
```

### `int()`

`int()` converts a value into an integer when possible.

For example:

```python
age = "26"

age = int(age)

print(age)
print(type(age))
```

Output:

```text
26
<class 'int'>
```

Before conversion:

```python
"26"
```

is a string.

After conversion:

```python
26
```

is an integer.

---

### `str()`

`str()` converts a value into a string.

```python
age = 26

age = str(age)

print(age)
print(type(age))
```

Output:

```text
26
<class 'str'>
```

Before conversion:

```python
26
```

is an integer.

After conversion:

```python
"26"
```

is a string.

---

## 9. What I Learned

In this lesson, I learned about:

* Variables
* Strings (`str`)
* Integers (`int`)
* Floating-point numbers (`float`)
* The `type()` function
* Basic arithmetic operators
* `int()` for converting values to integers
* `str()` for converting values to strings

I also used these concepts while working on my **bot v1.1**.

As I learn more Python, I will continue improving the bot and eventually update it to **v1.2**.
