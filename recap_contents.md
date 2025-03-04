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

**List**
* Lists are used to store multiple items in a single variable.
* Lists are created using square brackets.
* Lists are ordered, indexed, changeable and allow duplicate values.

~~~python
thislist = ["apple", "banana", "cherry"]
print(thislist)

#Lists allow duplicate values:

thislist = ["apple", "banana", "cherry", "apple", "cherry"]
print(thislist)

#Print the number of items in the list:

thislist = ["apple", "banana", "cherry"]
print(len(thislist))

#Using the list() constructor to make a List:

thislist = list(("apple", "banana", "cherry")) # note the double round-brackets
print(thislist)
~~~

**Access List Items**
* List items are indexed and you can access them by referring to the index number:
~~~python
#Print the second item of the list:

thislist = ["apple", "banana", "cherry"]
print(thislist[1])

#Print the last item of the list:

thislist = ["apple", "banana", "cherry"]
print(thislist[-1])

#Return the third, fourth, and fifth item (List Slicing):

thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[2:5])
~~~

**Change List Items**
* To change the value of a specific item, refer to the index number.
  
~~~python
#Change the second item:

thislist = ["apple", "banana", "cherry"]
thislist[1] = "blackcurrant"
print(thislist)

#Change a Range of Item Values
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "mango"]
thislist[1:3] = ["blackcurrant", "watermelon"]
print(thislist)
~~~
**Add List Items**

**Insert Method**
* To insert a new list item, without replacing any of the existing values, we can use the insert() method.
* The insert() method inserts an item at the specified index
  
~~~python
#Insert "watermelon" as the third item:

thislist = ["apple", "banana", "cherry"]
thislist.insert(2, "watermelon")
print(thislist)
~~~

**Append Method**
* To add an item to the end of the list, use the append() method.
* Using the append() method to append an item:

~~~python
thislist = ["apple", "banana", "cherry"]
thislist.append("orange")
print(thislist)
~~~

**Extend Method**
* To append elements from another list to the current list, use the extend() method.
* Add the elements of tropical to thislist:
  
~~~python
thislist = ["apple", "banana", "cherry"]
tropical = ["mango", "pineapple", "papaya"]
thislist.extend(tropical)
print(thislist)

#Add elements of a tuple to a list:

thislist = ["apple", "banana", "cherry"]
thistuple = ("kiwi", "orange")
thislist.extend(thistuple)
print(thislist)
~~~

**Remove List Items**
* The remove() method removes the specified item.
  
~~~python
#Remove "banana":

thislist = ["apple", "banana", "cherry"]
thislist.remove("banana")
print(thislist)

#Remove the first occurrence of "banana":

thislist = ["apple", "banana", "cherry", "banana", "kiwi"]
thislist.remove("banana")
print(thislist)

#The pop() method removes the specified index.
#Remove the second item:

thislist = ["apple", "banana", "cherry"]
thislist.pop(1)
print(thislist)

#Remove the last item:

thislist = ["apple", "banana", "cherry"]
thislist.pop()
print(thislist)

#The del keyword also removes the specified index:
#Remove the first item:

thislist = ["apple", "banana", "cherry"]
del thislist[0]
print(thislist)

#Clear the list content:

thislist = ["apple", "banana", "cherry"]
thislist.clear()
print(thislist)
~~~

**List Comprehension**
* List comprehension offers a shorter syntax when you want to create a new list based on the values of an existing list.
  
~~~python
newlist = [expression for item in iterable if condition == True]

fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = []

for x in fruits:
  if "a" in x:
    newlist.append(x)

print(newlist)

# With List Comprehension
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]

newlist = [x for x in fruits if "a" in x]

print(newlist)

#List Without Apple
newlist = [x for x in fruits if x != "apple"]
~~~

**Tuple**
* Tuples are used to store multiple items in a single variable.
* Tuples are ordered, unchangeable(immutable) and allow duplicate values.
* Tuples are written with round brackets. ()
Ex. mytuple = (“name”, “apple”)

~~~python
#Create a Tuple:

thistuple = ("apple", "banana", "cherry")
print(thistuple)

#Print the number of items in the tuple:

thistuple = ("apple", "banana", "cherry")
print(len(thistuple))

#Using the tuple() method to make a tuple:

thistuple = tuple(("apple", "banana", "cherry")) # note the double round-brackets
print(thistuple)

# NOTE: One item tuple, remember the comma:

thistuple = ("apple",)
print(type(thistuple))

#NOT a tuple
thistuple = ("apple")
print(type(thistuple))
~~~

**Access Tuple Items**
* You can access tuple items by referring to the index number, inside square brackets:
  
~~~python
#Print the second item in the tuple:
thistuple = ("apple", "banana", "cherry")
print(thistuple[1])

#Print the last item of the tuple:
thistuple = ("apple", "banana", "cherry")
print(thistuple[-1])

#Return the third, fourth, and fifth item:

thistuple = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
print(thistuple[2:5])
~~~

**Update Tuples**
* Tuples are unchangeable, meaning that you cannot change, add, or remove items once the tuple is created.
* But there are other steps to do that.
  
~~~python
#Convert the tuple into a list to be able to change it:

x = ("apple", "banana", "cherry")
y = list(x)
y[1] = "kiwi"
x = tuple(y)

print(x)

#Create a new tuple with the value "orange", and add that tuple:

thistuple = ("apple", "banana", "cherry")
y = ("orange",)
thistuple += y

print(thistuple)
~~~

**Remove Tuple Items**
* Tuples are unchangeable, so you cannot remove items from it, but you can use the same workaround as we used for changing and adding tuple items.

~~~python
#Convert the tuple into a list, remove "apple", and convert it back into a tuple:

thistuple = ("apple", "banana", "cherry")
y = list(thistuple)
y.remove("apple")
thistuple = tuple(y)

#The del keyword can delete the tuple completely:

thistuple = ("apple", "banana", "cherry")
del thistuple
print(thistuple) #this will raise an error because the tuple no longer exists
~~~

**Set**
* Sets are used to store multiple items in a single variable.
* Sets are unordered, unindexed, unchangeable( immutable) and do not allow duplicates.
* We can add and remove items only, modifying is not possible.
* Sets are written with curly brackets {} Ex.{“apple”, “mango”, “banana”}

~~~python
#Create a Set:

thisset = {"apple", "banana", "cherry"}
print(thisset)


#Using the set() constructor to make a set:

thisset = set(("apple", "banana", "cherry")) # note the double round-brackets
print(thisset)


#Duplicate values will be ignored:

thisset = {"apple", "banana", "cherry", "apple"}

print(thisset)


#True and 1 is considered the same value:

thisset = {"apple", "banana", "cherry", True, 1, 2}

print(thisset)


#False and 0 is considered the same value:

thisset = {"apple", "banana", "cherry", False, True, 0}

print(thisset)
~~~

**Access Set Items**
* You cannot access items in a set by referring to an index or a key.
* But you can loop through the set items using a for loop, or ask if a specified value is present in a set, by using the in keyword.

~~~python
#Loop through the set, and print the values:

thisset = {"apple", "banana", "cherry"}

for x in thisset:
  print(x)

#Check if "banana" is present in the set:

thisset = {"apple", "banana", "cherry"}

print("banana" in thisset)
~~~

**Add Set Items**
* Once a set is created, you cannot change its items, but you can add new items.
* To add one item to a set use the add() method.
  
~~~python
#Add an item to a set, using the add() method:

thisset = {"apple", "banana", "cherry"}

thisset.add("orange")

print(thisset)

# update() method
# To add items from another set into the current set, use the update() method.

# Add elements from tropical into thisset:

thisset = {"apple", "banana", "cherry"}
tropical = {"pineapple", "mango", "papaya"}

thisset.update(tropical)

print(thisset)
~~~

**Remove Set Items**
* To remove an item in a set, use the remove(), or the discard() method.
  
~~~python
#Remove "banana" by using the remove() method:

thisset = {"apple", "banana", "cherry"}

thisset.remove("banana")

print(thisset)


#Remove "banana" by using the discard() method:

thisset = {"apple", "banana", "cherry"}

thisset.discard("banana")

print(thisset)


#Remove a random item by using the pop() method:

thisset = {"apple", "banana", "cherry"}

x = thisset.pop()

print(x)

print(thisset)

#The del keyword will delete the set completely:

thisset = {"apple", "banana", "cherry"}

del thisset

print(thisset)
~~~
**Dictionary**
* Dictionaries are used to store data values in key:value pairs.
* A dictionary is a collection which is ordered, changeable and do not allow duplicate keys.
* Dictionaries are written with curly brackets, and have keys and values.
  
~~~python
#Create and print a dictionary:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict)

#Using the dict() method to make a dictionary:

thisdict = dict(name = "John", age = 36, country = "Norway")
print(thisdict)

#Duplicate values will overwrite existing values:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964,
  "year": 2020
}
print(thisdict)
~~~

**Access Dictionary Items**
* You can access the items of a dictionary by referring to its key name, inside square brackets:

~~~python
#Get the value of the "model" key:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
x = thisdict["model"]

#Using get() method, to get the value of the "model" key:

x = thisdict.get("model")

#The keys() method will return a list of all the keys in the dictionary.
#Get a list of the keys:

x = thisdict.keys()

#The values() method will return a list of all the values in the dictionary.
#Get a list of the values:

x = thisdict.values()

#The items() method will return each item in a dictionary, as tuples in a list.
#Get a list of the key:value pairs

x = thisdict.items()
~~~

**Change Dictionary Items**
* You can change the value of a specific item by referring to its key name

~~~python
#Change the "year" to 2018:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict["year"] = 2018

#Update the "year" of the car by using the update() method:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.update({"year": 2020})
~~~

**Add Dictionary Items**
* Adding an item to the dictionary is done by using a new index key and assigning a value to it.
  
~~~python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict["color"] = "red"
print(thisdict)


#Add a color item to the dictionary by using the update() method:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.update({"color": "red"})
~~~

**Remove Dictionary Items**
* There are several methods to remove items from a dictionary like pop(key), popitem() and del().

**pop() method**
~~~python
#The pop() method removes the item with the specified key name:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.pop("model")
print(thisdict)
~~~

**popitem() method**
~~~python
#The popitem() method removes the last inserted item:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.popitem()
print(thisdict)
~~~

**del keyword**
~~~python
#The del keyword removes the item with the specified key name:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
del thisdict["model"]
print(thisdict)
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

**Python Functions**
* A function is a block of code which only runs when it is called.
* You can pass data, known as parameters, into a function.
* A function can return data as a result.

**## Creating a Function**
* In Python a function is defined using the def keyword.
  
~~~python
def my_function():
  print("Hello from a function")

#To call a function, use the function name followed by parenthesis:

def my_function():
  print("Hello from a function")

my_function()
~~~

**Return Values**
* To let a function return a value, use the return statement.

~~~python
#Syntax: 

def function_name():
    statements
    .
    .
    return [expression]

def my_function(x):
  return 5 * x

print(my_function(3))
print(my_function(5))
print(my_function(9))
~~~

## **File Handling**

Python has some file modes :- 
* **r:** open an existing file for a read operation.
* **w:** open an existing file for a write operation. If the file already contains some data, then it will be overridden but if the file is not present then it creates a new file.
* **a:** open an existing file for append operation. It won’t override existing data.
* **x:** will create a file, returns an error if the file exist


Python has 4 file handling operations
* open()
* read()
* write()
* close()

**Reading a File/Read mode**
* we can read the content of a file in read mode.
  
~~~python
# The open command will open the Python file in the read mode and
# the for loop will print each line present in the file.

# 1. using the reading mode
def read_file(file_name):
    file = open(file_name, 'r')
    for data in file:
        print(data)

file = "geek.txt"
read_file(file)

# 2. read from any file using read() 
def read_file_1(file_name):
    file = open(file_name, 'r')
    return file.read()

file = "geek.txt"
read_file_1(file)
~~~

**Creating a File/Write mode**
* Let’s see how to create a file and how the write mode works.
  
~~~python
# create a file

def create_file(file_name, data):
    file = open(file_name, 'w')
    file.write(data)
    file.close()

file = "myfile.txt"
data = "hello python learners"

create_file(file, data)

~~~

**Working of Append Mode**
~~~python
# append to a file

def append_file(file_name, data):
    file = open(file_name, 'a')
    file.write(data)
    file.close()

file = "myfile.txt"
data = "This will add this line"

append_file(file, data)
~~~

## OOPS - Classes & Objects

* **Classes** - Blueprint to create an object
* **Objects** - Instance of a class

Objects - Car, Bus, Dog, Person, Laptop

Car Object - Methods and Variables/ Properties

Methods - accelerate(), brake(), speeddown() and speedup()

Properties - color, texture, material, brand name.


**Create a Class**

To create a class, use the keyword class
~~~python
class MyClass: 
  x = 5

#Create Object
#Now we can use the class named MyClass to create objects:

p1 = MyClass()
print(p1.x)

Output: 5

Ex:
class OopsConcept:
	Learner = “techie”
	Mentor = “basil”

P2 = OopsConcept()
P3 = OopsConcept()
print(p2.Mentor)
print(p3.Learner)
~~~

  
Create a class named person with parameters name and age
~~~python
class Person:
  def __init__(self, name, age): constructor
    self.name = name
	self.age = age

p1 = Person("John", 36)

print(p1.name)
print(p1.age)
~~~

## Pillars of OOP's
* Python Inheritance
* Python Polymorphism
* Python Encapsulation
* Python Abstraction

## PIP Installation

## Selenium
* Selenium is an open-source, automated testing tool used to test web applications across various browsers.
* Created in the year 2004 by Jason Huggins.
* Lets us write test scripts in programming languages like Python, Ruby, Java, PHP, Perl, JavaScript, and C#.
* Selenium enables to test your website on different browsers such as Google Chrome, Mozilla Firefox, Microsoft Edge, Safari, Internet Explorer (IE).
* Automated testing with Selenium can easily scale to cover a wide range of test cases, scenarios, and user interactions.
* This scalability ensures maximum test coverage of the application’s functionality.
* Selenium supports parallel test execution, allowing multiple tests to run concurrently.

## History of Selenium
![image](https://github.com/user-attachments/assets/1fcce4a2-4bd7-46bc-a48c-b10dcf887e7e)

## Advantages of Selenium
1. Language and Framework Support
2. Open Source Availability
3. Multi-Browser Support
4. Support Across Various Operating Systems
5. Ease of Implementation
6. Parallel test execution
7. Easy to Learn and Use

## Disadvantages of Selenium
1. Not support for mobile and desktop applications
2. Lack of built-in reporting
3. Maintenance efforts for test scripts
4. Dependency on browser updates
5. Not Having an Image Comparison
6. Not able to automate captchas and OTP's

**1. Selenium IDE**

**Selenium IDE helps in:**
* Creating automated test scripts and validating them at speed
* Identifying and highlighting errors during the replay of interactions
* Cross Browser Testing

**2. Selenium RC**
* Selenium RC was built to automate the testing of web applications by simulating user interactions across different browsers and platforms.
* It provided a way to browser automation remotely and execute test scripts written in various programming languages.
* Not supported and deprecated.

**3. Selenium WebDriver**
* Selenium WebDriver is a powerful and enhanced version of Selenium RC which was developed to overcome the limitations of Selenium RC.
* WebDriver communicates with browsers directly with the help of browser-specific native methods.
* Test the functionality of web applications by automating user interactions such as clicking buttons, filling out forms, navigating pages, and verifying expected outcomes.
* Test web application for consistency across different browsers and browser versions (e.g., Chrome, Firefox, Edge) 

**4. Selenium Grid**
* Selenium Grid is a component of the Selenium testing framework that allows you to run test scripts across multiple browsers, operating systems, and machines in parallel.
* It enables you to perform large-scale test automation and significantly reduces the time required for testing by executing tests simultaneously on different environments.

## Page Object Model - Automation Pytest
* A Page Object Model (POM) is a design pattern for writing clean and well structured codes.
* It is a way of using objects to represent elements on the page.
* Separate python classes are created to represent the web pages.
* This enables to write code that is simple and easy to understand.
* It also helps to keep our tests well-structured and understandable.

## Advantages of POM 
* The POM helps you write tests that are easy to understand and maintain.
* If something got changed on any page, we could easily find the functions and locators that need to be changed by that page class.
* The POM can help with collaboration between team members and improve the efficiency.
* Using POM, we can reuse our functions in different test scripts by importing them from Page Class.

## Project Explanation

When explaining your projects, especially in a technical interview or presentation, it's important to cover several key areas that help your audience understand not just what you built, but how and why you built it. Here are the main points you should cover:

### 1. Project Overview
- **Purpose & Objectives:** Explain the problem you aimed to solve and the goals of the project.
- **Context & Selection:** Discuss why this project is relevant and how it fits within a larger context (e.g., market need, academic research, personal learning).

### 2. Architecture & Design
- **Web Application:** Describe the high-level components of your project (e.g., frontend, backend, database) and how they interact.
- **Design Patterns:** Mention any design patterns or frameworks you used (e.g., MVC, Singleton, Factory, Page Object Model in testing).
- **Technology Stack:** List the programming languages, libraries, frameworks, and tools involved.

### 3. Implementation Details
- **Key Features & Functionality:** Highlight the main features of your project and explain how they work.
- **Code Structure:** Outline your project structure (modules, classes, functions) and justify your organizational choices.
- **Technical Challenges:** Discuss any complex issues you encountered and how you addressed them (e.g., performance bottlenecks, security considerations).

### 4. Testing & Quality Assurance
- **Testing Strategies:** Explain the testing approach (unit testing, integration testing, automation) and mention tools used (e.g., pytest, Selenium).
- **Error Handling & Logging:** Describe how you managed exceptions and maintained logs for debugging.
- **Continuous Integration (CI):** If applicable, explain how you integrated CI/CD tools to automate testing and deployment.

### 5. Results & Impact
- **Project Outcomes:** Share metrics or results that highlight the success of your project (e.g., performance improvements, user adoption).
- **User Feedback:** If available, include insights or testimonials from users.
- **Lessons Learned:** Reflect on what worked well, what didn’t, and what you would improve in future iterations.

### 6. Future Scope & Enhancements
- **Planned Improvements:** Discuss potential features or optimizations you would like to add.
- **Scalability & Maintenance:** Talk about how the project can be scaled or maintained over time.

