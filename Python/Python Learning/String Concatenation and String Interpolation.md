# Concatenating Strings

In Python, you can combine multiple strings together with the plus (+) operator. This process is called string concatenation. Here's how to concatenate two strings with the plus operator:

my_str_1 = 'Hello'
my_str_2 = "World"

str_plus_str = my_str_1 + ' ' + my_str_2
print(str_plus_str) # Hello World

# Repeating Strings

You can also repeat a string by multiplying it with an integer using the * operator. The string is repeated the specified number of times:

sound = 'ha'
repeated_sound = sound * 3
print(repeated_sound) # hahaha

# Concatenating Strings with Numbers

Concatenation only works with strings. If you try to concatenate a string with a number, you'll get a TypeError:

name = 'John Doe'
age = 26

name_and_age = name + age = TypeError: can only concatenate str (not "int") to str
This happens because Python does not automatically convert other data types like integers into strings when you concatenate them. Python requires all elements to be strings before it can concatenate them. To fix that, you can convert the number into a string with the built-in str() function, which returns the string representation of the given value without modifying the original value:

name = 'John Doe'
age = 26

name_and_age = name + str(age)
print(name_and_age) # John Doe26
You can also use the augmented assignment operator for concatenation. This is represented by a plus and equals sign (+=), and performs both concatenation and assignment in one step. Here it is in action:

name = 'John Doe'
age = 26

# String Interpolation

The process of inserting variables and expressions into a string is called string interpolation. Python has a category of string called f-strings (short for formatted string literals), which allows you to handle interpolation with a compact and readable syntax.

F-strings start with f (either lowercase or uppercase) before the quotes, and allow you to embed variables or expressions inside replacement fields indicated by curly braces ({}). Here's an example:

name = 'John Doe'
age = 26
name_and_age = f'My name is {name} and I am {age} years old'
print(name_and_age) # My name is John Doe and I am 26 years old

num1 = 5
num2 = 10
print(f'The sum of {num1} and {num2} is {num1 + num2}') # The sum of 5 and 10 is 15
Note how you don't need to convert non-string types with the str() function. In the example above, the value of the age, num1, and num2 variables is converted under the hood into a string during the interpolation process.

name_and_age = name  # Start with the name
name_and_age += str(age)  # Append the age as string

print(name_and_age)  # John Doe26
