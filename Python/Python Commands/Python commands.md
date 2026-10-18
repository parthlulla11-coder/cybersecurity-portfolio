Puthon commands - 

* **Print()** = Used to print a defined value like intiger, or float or string(for strings use ""). **Ex** - Print("hello world!")

* **Variables** = there are to store specific values or hold a data type as a memory we can use comma for defining multiple strings as different vaules **EX** - Name = Parth Age = 77 If we use the print(Age, Name)

* **input()** = we can use this funciton for the user to input any vaule and also we can store that inputr as a memory using variable function. 

* **if else** = can be used as a logical reasoning if the output is a then print ("hi") or else print("No") or end to terminate the program can be used with input and print. 

* **Boolean** = we can define the value if it's true or not like else if bu stating the value true it will return a specific value or if not then it will return another value. 

* **Type()** = this is used to define the type of the data we are dealing with like boolian, float, intiger, string etc. 

* **isinstance()** = lets you check if a variable matches a specific data type. It takes a value and the type you want to check it against, then returns a boolean.

* **in** =  which returns a boolean that specifies whether the character or characters exist in the string or not.

* **len()** = To get the length of a string.

* **square brackets ([])** = Each character in a string has a position called an index. The index is zero-based, meaning that the index of the first character of a string is 0, the index of the second character is 1, and so on. To access a character by its index, you use square brackets ([]) with the index of the character you want to access inside. Negative indexing is also allowed, so you can get the last character of any string with -1, the second-to-last character with -2.   

* **(+) operator** = In Python, you can combine multiple strings together with the plus (+) operator. This process is called string concatenation.

* operator = You can also repeat a string by multiplying it with an integer using the * operator. The string is repeated the specified number of times. 

* **str()** = Python does not automatically convert other data types like integers into strings when you concatenate them. Python requires all elements to be strings before it can concatenate them. To fix that, you can convert the number into a string with the built-in str() function, which returns the string representation of the given value without modifying the original value. 

Example of str() - 

name = 'John Doe'
age = 26

name_and_age = name + str(age)
print(name_and_age) 

Output = John Doe26

* **(+=)** = You can also use the augmented assignment operator for concatenation. This is represented by a plus and equals sign (+=), and performs both concatenation and assignment in one step.

Example - 

name = 'John Doe'
age = 26

name_and_age = name  # Start with the name
name_and_age += str(age)  # Append the age as string

print(name_and_age)  

**Output**  =  John Doe26

* **String Interpolation** 

The process of inserting variables and expressions into a string is called string interpolation. Python has a category of string called f-strings (short for formatted string literals), which allows you to handle interpolation with a compact and readable syntax.

F-strings start with f (either lowercase or uppercase) before the quotes, and allow you to embed variables or expressions inside replacement fields indicated by curly braces ({}).

<img width="752" height="371" alt="image" src="https://github.com/user-attachments/assets/c08b74b8-f548-4df2-8344-d11d30cda55f" />



