# Intermediate Python samples Python Functions

### Intermediate Python samples
### Python Functions
Functions in Python are reusable blocks of code that perform specific
tasks. They allow for modular and organized programming. Here are two
examples showcasing the use of functions in Python:

Simple Function:

```python
def greet(name):
  print("Hello, " + name + "!")

greet("Alice") 
#output: Hello, Alice!
```

In this example, a function named greet is defined, which takes a
parameter name and prints a greeting message with the given name.

We can rewrite the print statement to use "f-strings" and make this
prettier.

```python
def greet(name):
  print(f"Hello, {name}!")

greet("Alice") 
#output: Hello, Alice!
```

Function with Return Value:

```python
def add_numbers(a, b):
  return a+b

result = add_numbers(3,5)
print(result) #Output: 8
```

Here, the add_numbers function takes two parameters a and b and returns
their sum. The returned value is stored in the result variable and
printed.

Functions enable code reusability, enhance readability, and promote
modular programming in Python. They encapsulate functionality and allow
for efficient and structured development.

### Python Lambda
Lambda functions, also known as anonymous functions, are small, one-line
functions without a name. They are defined using the lambda keyword and
are typically used for simple and concise operations. Here are two
examples showcasing the use of lambda functions in Python:

Lambda Function with a Single Parameter:

``` 
square = lambda x: x**2
print(square(5)) # Output: 25
```

In this example, a lambda function square is defined to calculate the
square of a number x. The lambda function is then invoked with the
argument 5 and its result is printed.

Lambda Function with Multiple Parameters:

``` 
multiply = lambda x, y: x * y
print(multiply(3,4)) # Output: 12
```

Here, a lambda function multiply is defined to multiply two numbers x
and y. The lambda function is invoked with arguments 3 and 4, and the
result is printed.

Lambda functions provide a concise way to define small, anonymous
functions in Python. They are often used in situations where a function
is needed for a specific operation, without the need for a formal
function definition.

### Python Arrays
Arrays in Python are used to store multiple values of the same data type
in a single variable. Although Python does not have a built-in array
type, the array module provides an array-like object. Here are two
examples showcasing the use of arrays in Python:

Array Creation and Access:

```python
import array

numbers = array.array('i', [1,2,3,4,5])
print(numbers[0]) # Output: 1
pring(numbers[2]) # Output: 3
```

In this example, an array named numbers is created using the array
module. It stores signed integers ('i') and contains the specified
elements. Elements in an array are accessed using their respective
indices.

1.  [Array Operations:]

```python
import array

grades = array.array('f', [85.5, 90.2, 92.9])
grades.append(88.9)
grades.remove(90.2)
print(grades)
#Output: array('f', [85.5, 92.8, 88.9])
```

Here, the append() method adds an element to the end of the array, and
the remove() method removes a specific element from the array. The
modified array is printed to show the result.

Although arrays in Python are not as commonly used as lists, they offer
a more memory-efficient way to store large collections of homogeneous
data.

### Python Classes/Objects
Classes in Python are blueprints for creating objects, which are
instances of a class. They encapsulate data and functionality into a
single entity. Here are two examples showcasing the use of classes and
objects in Python:

1.  [Class Definition and Object Creation:]

```python
class Person:
  def __init__(self, name, age):
    self.name=name
    self.age=age

person1 = Person("John", 25)
person2 = Person("Alice", 30)
print(person1.name) #Output: John
priint(person2.age) #Output: 30
```

In this example, a class named Person is defined with a constructor
(\_\_init\_\_) method. Objects person1 and person2 are created based on
the class, with specific attributes. The attributes are accessed using
dot notation.

1.  [Class Methods:]


Here, the Rectangle class has a method named calculate_area that
calculates the area based on the width and height attributes of the
object. The method is called on the rect object, and the result is
printed.

Classes and objects provide a way to create reusable and organized code
structures in Python. They enable the implementation of object-oriented
programming principles such as encapsulation, inheritance, and
polymorphism.

### Python Inheritance
Inheritance is a fundamental concept in object-oriented programming that
allows a class to inherit attributes and methods from another class.
Here are two examples showcasing the use of inheritance in Python:

1.  [Single Inheritance:]


In this example, the Dog class inherits from the Animal class. The Dog
class overrides the speak method, providing a different implementation.
The dog object, created from the Dog class, invokes the speak method.

1.  [Multiple Inheritance:]


Here, the class C inherits from both classes A and B. As a result, the
object c can access and invoke methods from both parent classes.

Inheritance allows for code reuse, extensibility, and the creation of
hierarchies in object-oriented programming. It promotes modularity and
facilitates the implementation of complex systems by building upon
existing classes.

### Python Iterators
Iterators in Python are objects that allow for iterating over a
collection of elements or values. They implement the iterator protocol,
which requires the presence of the \_\_iter\_\_() and \_\_next\_\_()
methods. Here are two examples showcasing the use of iterators in
Python:

1.  [Custom Iterator:]


In this example, a custom iterator MyIterator is defined, which iterates
over the elements of my_list. The \_\_iter\_\_() method returns the
iterator object itself, and \_\_next\_\_() method retrieves the next
element in each iteration.

1.  [Built-in Iterator:]


Here, the built-in iter() function is used to obtain an iterator from
my_list, and the next() function retrieves the next element from the
iterator. Multiple calls to next() iterate over the remaining elements.

Iterators provide a way to traverse collections and process each element
individually. They offer flexibility and efficiency in handling large
data sets or generating values on the fly.

### Python Polymorphism
Polymorphism in Python refers to the ability of objects of different
classes to respond to the same method or function call. It allows for
the same code to be used with different types of objects, promoting code
reusability and flexibility. Here are two examples showcasing
polymorphism in Python:

1.  [Polymorphism with Inheritance:]


In this example, the speak() method is defined in the base Animal class
and overridden in the derived Dog and Cat classes. The loop iterates
over different objects, calling the speak() method, which behaves
differently based on the object type.

1.  [Polymorphism with Functions:]


Here, the area() function accepts an object as an argument and calls its
calculate_area() method. The function can work with different shapes,
such as Rectangle or Circle, as long as they have a compatible method.

Polymorphism allows for writing generic code that can handle multiple
object types, enhancing flexibility and extensibility in Python
programs. It promotes code reuse and simplifies the implementation of
complex systems.

### Python Scope
Scope in Python refers to the visibility and accessibility of variables,
objects, and functions within a program. Python follows a specific set
of rules to determine the scope of identifiers. Here are two examples
showcasing scope in Python:

1.  [Global Scope:]


In this example, the variable x is defined in the global scope, making
it accessible within the my_function() function.

1.  [Local Scope:]


Here, the variable y is defined within the local scope of the
my_function() function. It is accessible only within the function, and
attempting to access it outside of the function results in a NameError.

Understanding scope is crucial for variable visibility and avoiding
naming conflicts in Python programs. Local variables have precedence
over global variables within the same scope, and variables created
within a function are considered local to that function.

### Python Modules
Modules in Python are files containing Python code that can be imported
and used in other Python programs. They enable code organization,
reusability, and modularity. Here are two examples showcasing the use of
modules in Python:

Creating and Importing a Module:

1.  [Create a file named my_module.py with the following code:]


In another Python file, import and use the module:


1.  [Importing Specific Functions or Variables from a Module:]


In this example, specific functions (sqrt()) and a variable (pi) are
imported from the math module, allowing direct access to those elements
without specifying the module name.

Modules facilitate code reuse, organization, and encapsulation of
functionality in Python. They provide a way to divide programs into
smaller, manageable components that can be easily imported and utilized.

### Python Dates
In Python, dates are managed through the datetime module, which provides
classes for working with dates and times. Here are two examples
showcasing the use of dates in Python:

1.  [Current Date and Time:]


In this example, the date.today() function returns the current date,
while datetime.now().time() returns the current time with microseconds.

1.  [Date Formatting and Arithmetic:]


Here, a date string is formatted into a datetime object using
strptime(). The timedelta() function is used to perform date arithmetic,
adding 7 days to the formatted date.

Python's datetime module provides powerful tools for working with dates,
allowing operations like date formatting, arithmetic, comparison, and
more. It is extensively used in applications involving scheduling,
time-sensitive data, and date calculations.

### Python Math
Python's math module provides a range of mathematical functions and
constants for performing mathematical operations. Here are two examples
showcasing the use of the math module in Python:

1.  [Trigonometric Functions:]


In this example, the math.sin() and math.cos() functions are used to
calculate the sine and cosine values of an angle in radians.

1.  [Exponential and Logarithmic Functions:]


Here, the math.exp() function calculates the exponential value of 2,
while math.log() calculates the logarithm of 10 with base 2.

The math module provides a wide range of mathematical functions,
including square root, rounding, power, factorial, and more. It enables
precise mathematical computations and is frequently used in scientific,
engineering, and mathematical applications in Python.

### Python JSON
JSON (JavaScript Object Notation) is a lightweight data interchange
format that is widely used for data storage and communication. In
Python, the json module provides functions for working with JSON data.
Here are two examples showcasing the use of JSON in Python:

1.  [JSON Encoding:]


In this example, the json.dumps() function is used to encode the Python
dictionary data into a JSON-formatted string.

1.  [JSON Decoding:]


Here, the json.loads() function is used to decode the JSON string
json_data into a Python dictionary, allowing access to individual data
elements.

The json module in Python provides a convenient way to work with JSON
data, allowing for encoding and decoding of JSON strings and files. It
is commonly used in web APIs, data storage, and interchanging data
between different systems.

### Python RegEx
RegEx (Regular Expression) is a powerful tool for pattern matching and
text manipulation in Python. The re module in Python provides functions
for working with regular expressions. Here are two examples showcasing
the use of RegEx in Python:

1.  [Pattern Matching:]


In this example, the re.findall() function is used to find all
occurrences of one or more digits in the given text using the regular
expression \\d+.

1.  [Text Substitution:]


Here, the re.sub() function is used to substitute the occurrences of the
pattern "World" with the replacement text "Python" in the given text.

Regular expressions provide a powerful and flexible way to search,
match, and manipulate textual data in Python. They are widely used for
tasks such as data validation, text extraction, data cleaning, and more.

### Python PIP
PIP (Python Package Installer) is the standard package manager for
Python that allows you to install, manage, and uninstall Python packages
from the Python Package Index (PyPI) and other package repositories.
Here are two examples showcasing the use of PIP in Python:

1.  [Installing Packages:]


This command installs the specified package from PyPI or a custom
package repository.

1.  [Listing Installed Packages:]


This command displays a list of installed packages along with their
versions.

PIP simplifies package management in Python by providing an easy way to
install and manage third-party packages. It streamlines the process of
incorporating external libraries into Python projects, enhancing
functionality and productivity.

### Python Try...Except
The try...except block in Python is used to handle exceptions and
gracefully manage errors in code. It allows you to catch and handle
specific exceptions that may occur during the execution of a program.
Here are two examples showcasing the use of try...except in Python:

1.  [Handling Specific Exceptions:]


In this example, the code inside the try block raises a
ZeroDivisionError. The except block catches the exception and executes
the specified code, printing a custom error message.

1.  [Handling Multiple Exceptions:]


Here, the try block attempts to open a non-existent file and read its
content. The except blocks catch the FileNotFoundError and IOError
exceptions separately, allowing specific error handling for each case.

The try...except block helps prevent program crashes and provides an
opportunity to handle exceptions gracefully, improving the robustness of
Python programs. It allows for different error handling strategies based
on the type of exception encountered during execution.

### Python User Input
Python allows you to interact with users by accepting input from them
during program execution. Here are two examples showcasing how to take
user input in Python:

1.  [Taking User Input as a String:]

``` 
name = input("Enter your name: ")
print(f"Hello, {name}!")
```

In this example, the input() function is used to prompt the user to
enter their name. The input is stored in the variable name and is then
used to display a personalized greeting.

Taking User Input as an Integer:

``` 
age = int(input("Enter your age: "))
next_year = age + 1
print(f"Next year, you will be {next_year}!")
#Output: Next year, you will be 30!
```

Here, the user is prompted to enter their age. The input() function
returns a string, which is then converted to an integer using the int()
function. The age is incremented by 1 and displayed as the user's age
next year.

By utilizing user input, Python programs can be made more interactive
and dynamic, allowing users to provide data and influence program
behavior. It is important to handle user input validation and error
checking to ensure the input is of the expected type and format.

### Python String Formatting
String formatting in Python allows you to construct strings by embedding
values of variables or expressions within them. Here are two examples
showcasing string formatting in Python:

1.  [Using f-strings:]

``` 
name = "Alice"
age = 25
message = f"My name is {name} and I am {age} years old."
print(message) # Output: My name is Alice and I am 25 years old.
```

In this example, the f-string format allows you to embed variable values
directly within the string using curly braces {}. The variables name and
age are replaced with their corresponding values in the resulting
string.

1.  [Using the format() method:]

``` 
product = "Apple"
price = 0.99
quantity = 5
message = "I bought {} {}s for a total cost of ${:.2f}.".format(quantity, product, price * quantity)
print(message)
```

Here, the format() method is used to insert values into the string. The
curly braces {} act as placeholders for the variables, and their values
are provided as arguments to the format() method.

String formatting provides a convenient way to create dynamic and
expressive strings in Python. It allows for the inclusion of variables,
expressions, and formatting options within the string, making it
versatile for generating output and displaying information.

### Related Stories
- [[Python for Business Analysis: A Beginner's Guide (part
  1)](https://medium.com/@kylejones_47003/python-for-business-analysis-a-beginners-guide-part-1-50dc74a912e8)]
- [[Getting started with
  Python](https://medium.com/gitconnected/getting-started-with-python-62f689a0fb2c)]
- [[Why analytics is
  hard](https://medium.com/@kylejones_47003/why-analytics-is-hard-4c4b8c164821)]
::::::::By [Kyle Jones](https://medium.com/@kyle-t-jones) on
[June 20, 2023](https://medium.com/p/87f652402606).

[Canonical
link](https://medium.com/@kyle-t-jones/intermediate-python-sam-87f652402606)

Exported from [Medium](https://medium.com) on November 10, 2025.
