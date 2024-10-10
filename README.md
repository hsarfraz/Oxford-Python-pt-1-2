# Oxford-Python-pt-1-2

I have attached the assignments that I submitted for the Oxford University Department for Continuing Education Python courses (part 1 & 2). Part 1 of the course was a introduction to python programming, where I learned how to deal with structured and unstructured data using python. Part 2 focused on machine learning, deep learning and natural language processing using python. 

# Python Programming for Data Science - Part 1 Syllabus Overview

## Week 1: Introduction to Data Science. Introduction to Git and the Anaconda environment
[Week 1 Assignment](https://github.com/hsarfraz/Oxford-Python-pt-1-2/blob/main/1.1_week1_assignment.ipynb)

* Where Python is used (**bolded** words are projects I need to try)
  * Web Dev: Frameworks such as Django & Flask
  * **Data Analysis**: Libraries such as **NumPy**, **Pandas**, **Matplotlib**
  * **Internet of Things**: **Raspberry pi**, **TinyML IoT Devices**
  * Web Scraping: Scrapy
  * Computer Vision: OpenCV
  * **Machine Learning**: **Sci-kit Learn**, NLTK, **TensorFlow**
  * Game Dev: PyGame

### Variable Types in Python

* Numeric Types
  * int: These are whole numbers (ex. 10, 30, 40, etc.)
  * float: These are decimal numbers (ex. 10.6, 4.5, 67.8, etc.)
* Text Types
  * str: words and sentences (ex. 'Hello', 'Nick', etc.)
* Boolean Types
  * bool: True of False values -keep note of the uppercase
* NoneType 
  * NoneType: used to represent nothing -called None

### Different ways to print outputs (print w/ commas vs. concatenation)

* print w/ commas -a space is automatically assigned
  * Input: `print("Hello", "World)`
  * Output: Hello World
* concatenation: joining two statements together -a space is not assigned
  * Input: `print("Hello" + "World)`
  * Output: HelloWorld

### Static vs. Dynamic Languages

* Python is **dynamically typed** (type checked at run-time). The variables can initially be assigned a value of one type, and then be reassigned a value of a different type
* **Statically typed** languages (ex. C, C++, C#, Java) checks types at compile-time and only allows values of the same type to be assigned

### Sequence, Selection, Iteration

* Sequence: When each statement is executed by order (ie. line by line)
* Selection: Conditional statements that will only execute a block of code once, if it is true
* Iteration: Can repeat certain statements within a block, while the statement is true

## Week 2: Python basics: built-in types, functions and methods, if statement
[Week 2 Assignment](https://github.com/hsarfraz/Oxford-Python-pt-1-2/blob/main/1.2_week2_assignment.ipynb)

Week 2 will focus on these topics:
* Selection
* Operators
  * Comparison
  * Arithmetic
  * Logical
* Iteration
* Functions 

Selection in Python (if-then-else statements)
* Selection is when Python chooses to execute a certain line of code based on the condition given in the if-then-else statement
* Other languages: C, C++, C# and Java feature a switch statement and a ternary (?) operator as alternative ways to select between blocks of code
* Switch is not present in Python, not is '?' used

Comparison Operators
* `>` | Greater than
* `<` | Less than
* `>=` | Greater than or Equal
* `>=` | Less than or Equal
* `==` | Equality
* `!=` | Not Equal

Arithmetic Operators
* `+` | Addition
* `-` | Subtraction
* `/` | Division
* `%` | Modulus (Gives the remainder from division)
* `*` | Multiplication
* `//` | Floor Division (rounds down in a decimal value. So 4.3 -> 4 and -4.3 -> -5)
* `**` | Power of

Logical/Boolean Operators (NOT bitwise opperators such as `&` and `|`)
* `and` | logical AND
* `or` | logical OR
* `not` | logical NOT

Iteration in Python
* while loops: the loop will keep on going until the condition specified becomes false
 ```
i = 0
while i < 3:
 print('Loop', i)
 i = i + 1
#Output: 0, 1, 2
```
* for loops: the loop will execute the code under it until the range completes
 ```
for i in range(1,4):
 print(i)
#Output: 1, 2, 3
```

Functions in Python
* A function is a block of code that performs a well defined task
 ```
def get_input():
 return input('Please enter your name: ')

name = get_input()
print(name)
```
## Week 3: Python data structures: list, dictionaries, tuples; for...in loops

Content Overview
* Concept of Data Structures
 * Arrays
 * String
 * Lists
 * Tuples
 * Sets
 * Dictionaries

Data Structures
* Unlike a variable, which stores one value at a time, a data structure is built to store a collection of values
* **Indexed Structures** allow for random access (RAM) which allows a item to be located by the index location
* **Non-indexed Structures** (referenced structures), on the other hand, are navigated sequentially.

Arrays
* Elements: The items in an array
* Index: This is the numbering of elements inside a array
* When defining an array it is important to declare the size of the array (how many elements it would store) 
* Arrays can only store data **of the same type** that mentioned when declaring the array

Strings (str)
* Each string object is an immutable/fixed array of characters
* Each character is a numbered position in the array (index)
 * The numbering of the index starts at zero (ex. for the word "nick" the index would be n=0 i=1 c=2 k=3)

Exploring more functions/methods for a class (str, int, etc.)
* you can use the `dir()` function to get a list of the different types of functions/methods that you can use for that class (ex. `dir(str)` will return a list of methods that you can use on string classes, and example is the method `.find()` which will give you the position of a certain character)

```
name = "nick"
name.find('c')
#output: 2
```
Lists in Python


## Week 4: NumPy

## Week 5: Pandas for data science I 

## Week 6: Pandas for data science II

## Week 7: Matplotlib for Data visualisation

## Week 8: Object-oriented programming: classes, inheritance, and applications 

## Week 9: Data gathering and cleaning. Text pre-processing for Natural Language Processing (NLP)

## Week 10: Introduction to experimental design
