Python Notes — Functions & Strings
1. Functions

A function is something Python uses to perform a specific task.

For example, print() is a built-in Python function used to display something on the screen.

print("Hello world")

Here:

print() → the function
"Hello world" → the string we want to print
2. Strings

A string is text in Python.

Strings are written inside quotation marks:

"Hello world"

Examples:

"Hello"
"Python"
"My name is Parth"
"123"

Even "123" is a string because it is inside quotation marks.

3. Using a String with print()

We put the string inside the parentheses of the print() function:

print("Hello world")

Breakdown:

print()       → function
"Hello world" → string
4. Multi-line Strings

If you want to write text across multiple lines, you can use triple quotation marks:

print("""Hi, my name is Parth.
I'm new to Python.""")

Output:

Hi, my name is Parth.
I'm new to Python.

Triple quotes:

"""
text
"""

allow the string to contain multiple lines.

5. Combining Multiple Strings

You can put multiple strings next to each other:

print("Hi, my name is Parth, " "I'm new to Python " "This shit is fun!")

Python combines them into one line.

The spaces inside the quotation marks are important:

"Parth, "

The space before the closing " makes sure the next string doesn't stick directly to the previous word.

Output:

Hi, my name is Parth, I'm new to Python This shit is fun!
Cleaner way

You can also combine strings using +:

print("Hi, my name is Parth, " + "I'm new to Python " + "This shit is fun!")
Quick Notes
print() → a function that displays something on the screen.
String → text surrounded by quotation marks.
"Hello world" → a string.
print("Hello world") → uses the print() function to display a string.
""" """ → triple quotes, useful for multi-line strings.
Multiple strings → can be placed together or joined using +.
Spaces matter when combining strings.
