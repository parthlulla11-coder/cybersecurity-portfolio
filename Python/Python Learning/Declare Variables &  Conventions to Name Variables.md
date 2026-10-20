**In Python, variables are like labeled boxes for storing and referencing data of different types. To create a variable, write its name on the left, followed by the assignment (=) operator and the value you want to store on the right.**

**Following Naming Rules - **


* Variable names can only start with a letter or an underscore (_), not a number.
* Variable names can only contain alphanumeric characters (a-z, A-Z, 0-9) and underscores (_).
* Variable names are case-sensitive: age, Age, and AGE are all considered unique.
* Variable names cannot be one of Python's reserved keywords such as if, class, or def.
* If you break any of those rules, your Python program will raise a SyntaxError. 

**Naming Conventions**

First, variable names should be in lowercase, with words separated by an underscore. This is called snake case: 

my_variable_name = 'freeCodeCamp'

Next, you should use descriptive names for variables. For example, if you want to save a user's age as a variable, user_age is better than age or an abbreviation like ua:

user_age = 30

This way, you can easily communicate the purpose of a variable to other team members (or to your future self) in a large codebase.

Another convention is to avoid using single-letter variable names. Single-letter names are common in Python, but they should be avoided because they communicate no purpose or meaning:

x = 56 # What do you mean by x?

Writing Comments
The pound symbol (#) and the text that follows it form a comment. Comments let you add notes and explanations to your code.

In Python, comments start with a pound symbol (#), and the language ignores everything after the # symbol on that line:

# This is a single-line comment
Multi-line comments can be created by using consecutive single-line comments:

# This is a
# multi-line
# comment
You can use comments to explain your code, leave reminders for yourself, or clarify why a line exists. Comments are especially helpful when you're learning or working in teams.

However, you shouldn't use comments to explain what your variable names mean. Instead, the names you choose for your variables should be descriptive and communicate what they're for, and follow the other naming rules mentioned earlier to prevent syntax errors.

