## Module 1 Cheat Sheet: Python Basics

| Package/Method	| Description  | Code Example |
|------------|------------|------------|
| Comments   | Comments are lines of text that are ignored by the Python interpreter when executing the code<./td>   | # This is a comment  |
| Concatenation  | Combines (concatenates) strings.   |Syntax: 1 concatenated_string = string1 + string2  Example: 1 result = "Hello" + " John"</td>   |
| Data Types  | - Integer - Float - Boolean - String | Example: 1 x=7  # Integer Value 2 y=12.4  # Float Value 3 is_valid = True  # Boolean Value  4 is_valid = False  # Boolean Value  5 F_Name = "John" # String Value |
| Indexing | Accesses character at a specific index. | Example: 1 my_string="Hello" / 2 char = my_string[0] |
| len()	| Returns the length of a string. | Syntax: 1 len(string_name)  Example: 1 my_string="Hello"  / 2 length = len(my_string) |
| lower()	| Converts string to lowercase.	 | Example: 1 my_string="Hello" / 2 uppercase_text = my_string.lower() |
| print()	 | Prints the message or variable inside `()`.	 | Example: 1 print("Hello, world")  / 2 print(a+b) |
| Python Operators	| - Addition (+): Adds two values together. - Subtraction (-): Subtracts one value from another. - Multiplication (*): Multiplies two values. - Division (/): Divides one value by another, returns a float. - Floor Division (//): Divides one value by another, returns the quotient as an integer. - Modulo (%): Returns the remainder after division | Example: 1 x = 9 y = 4 / 2 result_add= x + y # Addition  / 3 result_sub= x - y # Subtraction / 4 result_mul= x * y # Multiplication / 5 result_div= x / y # Division  / 6 result_fdiv= x // y # Floor Division / 7 result_mod= x % y # Modulo</td> |
| replace()	 | Replaces substrings.	| Example: 1 my_string="Hello"  / 2 new_text = my_string.replace("Hello", "Hi") |
| Slicing	 | Extracts a portion of the string.	| Syntax: 1 substring = string_name[start:end] // Example: 1 my_string="Hello" substring = my_string[0:5] |
| split()	 | Splits string into a list based on a delimiter.	| Example: 1 my_string="Hello" / 2 split_text = my_string.split(",") |
| strip()	 | Removes leading/trailing whitespace.	 |  Example: 1 my_string="Hello" / 2 trimmed = my_string.strip() |
| upper()	 | Converts string to uppercase.	| Example: 1 my_string="Hello" / 2 uppercase_text = my_string.upper() |
| Variable Assignment	| Assigns a value to a variable.	| Syntax: 1 variable_name = value // Example: 1 name="John" # assigning John to variable name  /2 x = 5 # assigning 5 to variable x |
