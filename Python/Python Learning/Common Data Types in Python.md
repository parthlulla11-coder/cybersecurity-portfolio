Before working with Python variables, it's important to understand data types. A data type describes the kind of value a variable holds, for example, a number or a piece of text. Programming languages use data types so they know how to store and work with different kinds of information.

Python is a dynamically typed language. This means you do not specify a variable's data type when you create it. Python determines the type from the value assigned to the variable.

Here are some examples:

name = 'John Doe' # Python knows this is a string
age = 25 # Python knows this is an integer
A variable can later be assigned a value of a different type:

age = 25
age = 'Twenty-five'
After the second assignment, age contains a string instead of an integer.

For now, focus on four data types that you will use throughout this module:

Integer: A whole number without decimals, for example, 10 or -5.
my_integer_var = 10
print('Integer:', my_integer_var) # Integer: 10
Float: A number with a decimal point, like 4.41 or -0.4.
my_float_var = 4.50
print('Float:', my_float_var) # Float: 4.5
String: A sequence of characters enclosed in single or double quotation marks like 'Hello world!'.
my_string_var = 'hello'
print('String:', my_string_var) # String: hello
Boolean: A true or false type, written as True or False.
my_boolean_var = True
print('Boolean:', my_boolean_var) # Boolean: True
