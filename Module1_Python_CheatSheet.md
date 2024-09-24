# Python_basics_CheatSheet
 
Module 1 Cheat Sheet: Python Basics

## Package/Method	                                  Description	                                                             Code Example
Comments	                Comments are lines of text that are ignored by the Python 
                               interpreter when executing the code<./td>	                                             1# This is a comment
------------------------------------------------------------------------------------------------------------------------------------------------------
Concatenation	                             Combines (concatenates) strings.	                             Syntax:1concatenated_string = string1 + string2 
                                                                                                           Example:1 result = "Hello" + " John"</td>
Data Types	- Integer - Float - Boolean - String	Example:
1
2
3
4
5
6
7
8
9
10
x=7 
# Integer Value 
y=12.4 
# Float Value 
is_valid = True 
# Boolean Value 
is_valid = False 
# Boolean Value 
F_Name = "John" 
# String Value
Copied!
Indexing	Accesses character at a specific index.	Example:
1
2
my_string="Hello" 
char = my_string[0]
Copied!
len()	Returns the length of a string.	Syntax:
1
len(string_name) 
Copied!
Example:

1
2
my_string="Hello" 
length = len(my_string)
Copied!
lower()	Converts string to lowercase.	Example:
1
2
my_string="Hello" 
uppercase_text = my_string.lower()
Copied!
print()	Prints the message or variable inside `()`.	Example:
1
2
print("Hello, world") 
print(a+b)
Copied!
Python Operators	- Addition (+): Adds two values together.
- Subtraction (-): Subtracts one value from another.
- Multiplication (*): Multiplies two values.
- Division (/): Divides one value by another, returns a float.
- Floor Division (//): Divides one value by another, returns the quotient as an integer.
- Modulo (%): Returns the remainder after division.	Example:
1
2
3
4
5
6
7
x = 9 y = 4 
result_add= x + y # Addition 
result_sub= x - y # Subtraction 
result_mul= x * y # Multiplication 
result_div= x / y # Division 
result_fdiv= x // y # Floor Division 
result_mod= x % y # Modulo</td>
Copied!
replace()	Replaces substrings.	Example:
1
2
my_string="Hello" 
new_text = my_string.replace("Hello", "Hi")
Copied!
Slicing	Extracts a portion of the string.	Syntax:
1
substring = string_name[start:end] 
Copied!
Example:

1
my_string="Hello" substring = my_string[0:5]
Copied!
split()	Splits string into a list based on a delimiter.	Example:
1
2
my_string="Hello" 
split_text = my_string.split(",")
Copied!
strip()	Removes leading/trailing whitespace.	Example:
1
2
my_string="Hello" 
trimmed = my_string.strip()
Copied!
upper()	Converts string to uppercase.	Example:
1
2
my_string="Hello" 
uppercase_text = my_string.upper()
Copied!
Variable Assignment	Assigns a value to a variable.	Syntax:
1
variable_name = value 
Copied!
Example:

1
2
name="John" # assigning John to variable name 
x = 5 # assigning 5 to variable x
Copied!

© IBM Corporation. All rights reserved.

| Colonne 1  | Colonne 2  | Colonne 3  |
|------------|------------|------------|
| Valeur 1   | Valeur 2   | Valeur 3   |
| Valeur 4   | Valeur 5   | Valeur 6   |
| Valeur 7   | Valeur 8   | Valeur 9   |


