## 1. Python Fundamentals
Data Types & Variables, Control Structures, Functions & Modules,
Object-Oriented Programming, Error & Exception Handling, File Handling

**What is Python?**
* Python is an open source, high level, interpreted programming language. 
* It was developed by “Guido Van Rossum” and released in the year 1991.
  
**Why Python?**
* Python works on different platforms (Windows, Mac, Linux, etc).
* Python has a simple syntax similar to the English language.
* Python has syntax that allows developers to write programs with fewer lines than some other programming languages.
* Python runs on an interpreter system, meaning that code can be executed as soon as it is written. This means that prototyping can be very quick.

**Python Syntax**
* Python syntax can be executed by writing directly in the Command Line
~~~python
>>> print("Hello, World!")
Hello, World!
~~~

**Python Comments**
* Comments can be used to explain Python code.
* Comments can be used to make the code more readable.
* Comments can be used to prevent execution when testing code.

~~~python
#This is a comment
print("Hello, World!")

print("Hello, World!") #This is a comment

#print("Hello, World!")
print("Cheers, Mate!")
~~~

**Multiline Comments**
* Python does not really have a syntax for multiline comments.
~~~python
"""
This is a comment
written in
more than just one line
"""
print("Hello, World!")
~~~

**Variables in python?**
* Variables are containers to store data values.
* The data values will be String, Float, Tuple, List

**Data Types in Python**
* Python has the following data types built-in by default, in these categories:
~~~
Text Type:	str
Numeric Types:	int, float, complex
Sequence Types:	list, tuple, range
Mapping Type:	dict
Set Types:	set
Boolean Type:	bool
None Type:	NoneType
~~~

**Strings**
* Strings in python are surrounded by either single quotation marks, or double quotation marks.
* 'hello' is the same as "hello".

You can display a string literal with the print() function:
~~~python
print("Hello")
print('Hello')
~~~

**Assign String to a Variable**
* Assigning a string to a variable is done with the variable name followed by an equal sign and the string:
~~~python
a = "Hello"
print(a)
~~~

**String Length**
* To get the length of a string, use the len() function.
~~~python
a = "Hello, World!"
print(len(a))
~~~

**Check String**
* To check if a certain phrase or character is present in a string, we can use the keyword **in**.
* Check if "free" is present in the following text:
~~~python
mytext = "The best things in life are free!"
print("free" in mytext)
~~~

**Slicing Strings**
* You can return a range of characters by using the slice syntax.
* Specify the start index and the end index, separated by a colon, to return a part of the string.
  
~~~python
#Get the characters from position 2 to position 5 (not included):
b = "Hello, World!"
print(b[2:5])

#Get the characters from the start to position 5 (not included):
b = "Hello, World!"
print(b[:5])

#Get the characters from position 2, and all the way to the end:
b = "Hello, World!"
print(b[2:])

#Negative Indexing
#Use negative indexes to start the slice from the end of the string:
b = "Hello, World!"
print(b[-5:-2])

#Start, End, Step 
b = "Hello, World!"
print(b[::-1])

~~~

**Modify Strings**
* Python has a set of built-in methods that you can use on strings.
~~~python
#The upper() method returns the string in upper case:
a = "Hello, World!"
print(a.upper())

#The lower() method returns the string in lower case:
a = "Hello, World!"
print(a.lower())

#The strip() method removes any whitespace from the beginning or the end:
a = " Hello, World! "
print(a.strip()) # returns "Hello, World!"

#The replace() method replaces a string with another string:
a = "Hello, World!"
print(a.replace("H", "J"))

#The split() method splits the string into substrings if it finds instances of the separator:
a = "Hello, World!"
print(a.split(",")) # returns ['Hello', ' World!']
~~~

**String Concatenation**
* To concatenate, or combine, two strings you can use the + operator.
~~~python
#Merge variable a with variable b into variable c:
a = "Hello"
b = "World"
c = a + b
print(c)

#To add a space between them, add a " ":
a = "Hello"
b = "World"
c = a + " " + b
print(c)
~~~

**Format - Strings (f-strings)**
* We cannot combine strings and numbers like this.
* To specify a string as an f-string, simply put an 'f' in front of the string literal, and add curly brackets {} as placeholders for variables and other operations.
~~~python
age = 36
txt = "My name is John, I am " + age
print(txt)

age = 36
txt = f"My name is John, I am {age}"
print(txt)
~~~

**Python Numbers**
* There are three numeric types in Python:

1. int - Integer - Int, or integer, is a whole number, positive or negative, without decimals, of unlimited length.
2. float - Float - Float, or "floating point number" is a number, positive or negative, containing one or more decimals.
3. complex - Complex - Complex numbers are written with a "j" as the imaginary part.

* Variables of numeric types are created when you assign a value to them:
~~~python
x = 1    # int
y = 2.8  # float
z = 1j   # complex

print(type(x))
print(type(y))
print(type(z))
~~~

**Type Conversion**
* You can convert from one type to another with the int(), float(), and complex() methods:
~~~python
Convert from one type to another:

x = 1    # int
y = 2.8  # float
z = 1j   # complex

#convert from int to float:
a = float(x)

#convert from float to int:
b = int(y)

#convert from int to complex:
c = complex(x)

print(a)
print(b)
print(c)

print(type(a))
print(type(b))
print(type(c))
~~~

**Python Casting**
* Casting in python is therefore done using constructor functions:

int() - constructs an integer number from an integer literal, a float literal (by removing all decimals), or a string literal (providing the string represents a whole number)
float() - constructs a float number from an integer literal, a float literal or a string literal (providing the string represents a float or an integer)
str() - constructs a string from a wide variety of data types, including strings, integer literals and float literals
~~~python
x = int(1)   # x will be 1
x = float(1)     # x will be 1.0
x = str("s1") # x will be 's1'
~~~

**Python Operators**
* Operators are used to perform operations on variables and values.
* We use the + operator to add together two values:
~~~python
print(10 + 5)
~~~

**Operator Types**
Python divides the operators in the following groups:

* Arithmetic operators 
* Assignment operators
* Comparison operators
* Logical operators
* Identity operators
* Membership operators
* Bitwise operators

**Python Arithmetic Operators**
* Arithmetic operators are used with numeric values to perform common mathematical operations.
~~~
Examples
+	Addition	x + y	
-	Subtraction	x - y	
*	Multiplication	x * y	
/	Division	x / y	
%	Modulus	x % y	
**	Exponentiation	x ** y	
//	Floor division	x // y
~~~

**Python Assignment Operators**
* Assignment operators are used to assign values to variables.

~~~
Examples
=	x = 5	x = 5	
+=	x += 3	x = x + 3	
-=	x -= 3	x = x - 3	
*=	x *= 3	x = x * 3	
/=	x /= 3	x = x / 3
~~~

**Python Comparison Operators**
* Comparison operators are used to compare two values.

~~~
Examples
==	Equal	x == y	
!=	Not equal	x != y	
>	Greater than	x > y	
<	Less than	x < y	
>=	Greater than or equal to	x >= y	
<=	Less than or equal to	x <= y
~~~

**Python Logical Operators**
* Logical operators are used to combine conditional statements.

~~~
Examples
and 	Returns True if both statements are true	x < 5 and  x < 10	
or	Returns True if one of the statements is true	x < 5 or x < 4	
not	Reverse the result, returns False if the result is true	not(x < 5 and x < 10)

x = 5
print(not(x > 3 and x < 10))
~~~

**Python Identity Operators**
* Identity operators are used to compare the objects, not if they are equal, but if they are actually the same object, with the same memory location:

~~~
Examples
is 	Returns True if both variables are the same object	x is y	
is not	Returns True if both variables are not the same object	x is not y
~~~

**Python Membership Operators**
* Membership operators are used to test if a sequence is presented in an object

~~~
Examples
in 	Returns True if a sequence with the specified value is present in the object	x in y	
not in	Returns True if a sequence with the specified value is not present in the object	x not in y
~~~

**Python Bitwise Operators**
* Bitwise operators are used to compare (binary) numbers
~~~
Examples
& 	AND	Sets each bit to 1 if both bits are 1	x & y
print(6 & 3)
6 = 0000000000000110
3 = 0000000000000011
--------------------
2 = 0000000000000010
====================
~~~

**Python Conditional statements**
* An "if statement" is written by using the if keyword.
* Indentation - Python relies on indentation (whitespace at the beginning of a line) to define scope in the code.

~~~python
If statement:

a = 33
b = 200
if b > a:
  print("b is greater than a")
~~~

**Elif**
* The elif keyword is Python's way of saying "if the previous conditions were not true, then try this condition".

~~~python
a = 33
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
~~~

**Else**
The else keyword catches anything which isn't caught by the preceding conditions.

~~~python
a = 200
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
else:
  print("a is greater than b")
~~~

**Looping statements**
* Looping is used for iterating over a sequence (that is either a list, a tuple, a dictionary, a set, or a string).

**1. For Loop
2. While Loop**

**For Loop**
* With the for loop we can execute a set of statements, once for each item in a list, tuple, set etc.

~~~python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)

#looping through a string
for x in "banana":
  print(x)
~~~

**Break Statement**
* With the break statement we can stop the loop before it has looped through all the items:

~~~python
Exit the loop when x is "banana":

fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)
  if x == "banana":
    break

fruits = ["apple", "banana", "cherry"]
for x in fruits:
  if x == "banana":
    break
  print(x)
~~~

**Continue Statement**
* With the continue statement we can stop the current iteration of the loop, and continue with the next.

~~~python
#Do not print banana:

fruits = ["apple", "banana", "cherry"]
for x in fruits:
  if x == "banana":
    continue
  print(x)
~~~

**pass Statement**
* for loops cannot be empty, but if you for some reason have a for loop with no content, put in the pass statement to avoid getting an error.

~~~python
for x in [0, 1, 2]:
  pass
~~~

**range() Function**
* To loop through a set of code a specified number of times, we can use the range() function,
* The range() function returns a sequence of numbers, starting from 0 by default, and increments by 1 (by default), and ends at a specified number.
~~~python
for x in range(6):
  print(x)

for x in range(2, 6):
  print(x)

for x in range(2, 30, 3):
  print(x)
~~~

**Nested Loops XXX**
* A nested loop is a loop inside a loop.
* The "inner loop" will be executed one time for each iteration of the "outer loop".

~~~python
adj = ["red", "big", "tasty"]
fruits = ["apple", "banana", "cherry"]

for x in adj:
  for y in fruits:
    print(x, y)

Example 2 - Multiplication Table
for i in range(2, 4):

    # Printing inside the outer loop
    # Running inner loop from 1 to 10
    for j in range(1, 11):

        # Printing inside the inner loop
        print(i, "*", j, "=", i*j)
    # Printing inside the outer loop
    print()

Nested While Loop
x = [1, 2]
y = [4, 5]
i = 0
while i < len(x) :
  j = 0
  while j < len(y) :
    print(x[i] , y[j])
    j = j + 1
  i = i + 1
~~~

**while Loop**
* With the while loop we can execute a set of statements as long as a condition is true.

~~~python
i = 1
while i < 6:
  print(i)
  i += 1

#break
i = 1
while i < 6:
  print(i)
  if i == 3:
    break
  i += 1

#continue
i = 0
while i < 6:
  i += 1
  if i == 3:
    continue
  print(i)
~~~

