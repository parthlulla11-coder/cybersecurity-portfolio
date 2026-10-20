A string is a sequence of characters surrounded by either single or double quotation marks. Python treats both forms as strings, so you can use either one. Here are some examples:

my_str_1 = 'Hello'
my_str_2 = "World"
If you need a multiline string, you can use triple double quotes or triple single quotes:

my_str_3 = """Multiline
string"""
my_str_4 = '''Another
multiline
string'''
If your string contains either single or double quotation marks, then you have two options:

Use the opposite kind of quotes. That is, if your string contains single quotes, use double quotes to wrap the string, and vice versa:
msg = "It's a sunny day"
quote = 'She said, "Hello World!"'
Escape the single or double quotation mark in the string with a backslash (\). With this method, you can use either single or double quotation marks to wrap the string itself:
msg = 'It\'s a sunny day'
quote = "She said, \"Hello!\""
Sometimes, you may need to check if a string contains one or more characters. For that, Python provides the in operator, which returns a boolean that specifies whether the character or characters exist in the string or not.

Here are some examples:

my_str = 'Hello world'

print('Hello' in my_str)  # True
print('hey' in my_str)    # False
print('hi' in my_str)    # False
print('e' in my_str)  # True
print('f' in my_str)  # False
Now, let's look at how you can get the length of a string and work with the individual characters in a string, a process called indexing. To get the length of a string, you can use the built-in len() function. Here's an example:

my_str = 'Hello world'
print(len(my_str))  # 11
Each character in a string has a position called an index. The index is zero-based, meaning that the index of the first character of a string is 0, the index of the second character is 1, and so on. To access a character by its index, you use square brackets ([]) with the index of the character you want to access inside. Here are some examples:

my_str = "Hello world"

print(my_str[0])  # H
print(my_str[6])  # w
Negative indexing is also allowed, so you can get the last character of any string with -1, the second-to-last character with -2, and so on:

my_str = 'Hello world'
print(my_str[-1])  # d
print(my_str[-2]) # l
In Python, values can be mutable or immutable. A mutable value can be changed after it is created, while an immutable value cannot.

You can point a variable at a new value, which is called reassignment, but you can't change an immutable value itself by adding, removing, or replacing any of its elements.

Strings are immutable in Python, but you can still reassign a variable to a different string:

greeting = 'hi'
greeting = 'hello'
print(greeting) # hello
But direct modification of a string isn't allowed:

greeting = 'hi'
greeting[0] = 'H' # TypeError: 'str' object does not support item assignment
Integers, floats, and booleans are also immutable. You will learn about other immutable types in later lessons.
