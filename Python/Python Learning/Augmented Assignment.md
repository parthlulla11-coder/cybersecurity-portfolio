**Augmented assignment applies an operation to a variable and stores the result back in the same variable, all in one step.**

**The basic syntax of an augmented assignment looks like this:**

variable <operator>= value

# For numeric variables, this is a shorter way to write the following assignment:

**Example Code**

variable = variable <operator> value

For example, you can use augmented assignment to add 5 to an existing variable:

**Example Code**

my_var = 10
my_var += 5

print(my_var) # 15

And here is the same thing, but without augmented assignment:

**Example Code**

my_var = 10
my_var = my_var + 5

print(my_var) # 15

The advantage of augmented assignment is that it provides a concise and readable way to update a variable value without repeating the variable name. In turn, this reduces redundancy and potential errors that might arise from a typo or something similar.
Arithmetic and bitwise operators have augmented assignment forms. We've looked at the addition assignment operator (+=), so let's look at others.

# The subtraction assignment operator (-=) subtracts the right operand from the left variable and stores the difference in the left variable:

**Example Code**

count = 14
count -= 3

print(count) # 11

# The multiplication assignment operator (*=) multiplies the left variable by the right operand and stores the product back in the left variable:

**Example Code**

product = 65
product *= 7

print(product) # 455

# The division assignment operator (/=) divides the left variable by the right and stores the result back in the left variable:

Example Code

price = 100
price /= 4

print(price) # 25.0

# The floor division assignment operator (//=) floor‑divides the left variable by the right and stores the result back in the left variable:

Example Code

total_pages = 23
total_pages //= 5
print(total_pages) # 4

# The modulo assignment operator (%=) computes the remainder of the left variable divided by the right and stores it back in the left variable:

Example Code
bits = 35
bits %= 2

print(bits) # 1

# The exponentiation assignment operator (**=) raises the left variable to the power of the right and stores the result back in the left variable:

Example Code
power = 2
power **= 3

print(power) # 8

#You can use some augmented assignment operators with strings, too. For example, the addition assignment operator makes it easy to concatenate strings:

Example Code
greet = 'Hello'
greet += ' World'

print(greet) # Hello World

# The multiplication assignment operator can be used to repeat a string:

Example Code
greet = 'Hello'
greet *= 3

print(greet) # HelloHelloHello

# The subtraction and division assignment operators raise a TypeError when used with strings:

Example Code

greet = 'Hello'
greet -= ' World' # TypeError: unsupported operand type(s) for -=: 'str' and 'str'

Example Code

greet = 'Hello'
greet /= 'World' # TypeError: unsupported operand type(s) for /=: 'str' and 'st
