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

[Week 3 Assignment](https://github.com/hsarfraz/Oxford-Python-pt-1-2/blob/main/1.3_week3_assignment.ipynb)

Content Overview
* Concept of Data Structures
 * Arrays
 * String
 * `[,]` Lists (mutable, we can modify it by adding or removing things)
 * `(,)`Tuples (immutable)
 * `{,}` Sets (unique values, duplicates are not printed)
 * `{k:v}` Dictionaries (key and value pairs)

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
* A list in python does use the subscript operator `[]` typically associated with an array. Elements in the list are also indexed/numbered
* Lists in python are resizable, unlike static arrays which are fixed
* Python lists can store elements of different types, whereas arrays are declared to store values of one type

List Slicing
```
l = [1,2,3,4,5,6]
l[2:4]
#output: [3,4]
```

List Append
```
l = [1,2,3,4,5,6]
l.append(7)
#output: [1,2,3,4,5,6,7]
```

List Remove
```
l = [1,2,3,4,5,6]
l.remove(7)
#output: [1,2,3,4,5,6]
```

Tuples in Python
* Tuples are constant (immutable) which means that once they are declared they can't be reassigned
* Tuples are declared with `()`

Re-assignment not permitted in tuples
```
t = (1,2,3,4,5,6)
t[0] = 5
#output: 'tuple' object does not support item assignment
```

Tuple count method
```
t = (1,1,1,4,5,6)
t.count(1)
#output: 3
```

Tuple index method
```
t = (1,1,1,4,5,6)
t.index(5)
#output: 4
```

Sets in Python
* Sets in mathematics refer to a set of distinct numbers - there are no duplicates
* It is possible to store duplicates in a python set, but only unique values will be printed
* Sets are declared with `{}`
* Sets are mutable (can change)

Add to set
```
s = {1,2,3,4,5,6}
s.add{7}
#output: {1,2,3,4,5,6,7}
```

Set Duplicates
```
s = {1,2,3,4,5,6,1,2,3,4,5,6}
s
#output: {1,2,3,4,5,6}
```

Cast to set (convert list to set to see unique values)
```
l = [1,1,2,2,3,3,4,4,5,5,6,6]
s = set(l)
s
#output: {1,2,3,4,5,6}
```

Set Theory (the symbols used to execute the set theories below are known as bitwise opperators such as `&` and `|`)
* Intersect $A \cap B$: The common values in both sets
 ```
s1 = {1,2,3,4,5,6}
s2 = {4,5,6,7,8,9}
s1 & s2
#output: {4,5,6}
```
* Union ($A \cup B$): All values from both sets, including the common values
```
s1 = {1,2,3,4,5,6}
s2 = {4,5,6,7,8,9}
s1 | s2
#output: {1,2,3,4,5,6,7,8,9}
```
* Difference ($A - B$): Only includes the values of one set (no common values are included)
```
s1 = {1,2,3,4,5,6}
s2 = {4,5,6,7,8,9}
s1 - s2
#output: {1,2,3}
```

Dictionaries in Python
* Dictionaries in python need to be specified by a key (word) to be able to get a value (definition)
* Like a Set, dictionaries also use the `{}` but they include a colon to establish a key and value pair (ex. `{k:v}`)

Append to a Dictionary
```
d = {'USA': 200, 'UK': 150, 'EU': 2}
d['Asia'] = 30
d
#Output: {'USA': 200, 'UK': 150, 'EU': 2, 'Asia': 30}
```

Remove values from a Dictionary
```
d = {'USA': 200, 'UK': 150, 'EU': 2, 'Asia': 30}
del d['Asia'] 
d
#Output: {'USA': 200, 'UK': 150, 'EU': 2}
```

Dictionary Keys and Values
```
d = {'USA': 200, 'UK': 150, 'EU': 2}
print( d.keys() ) #Output: dict_keys(['USA', 'UK', 'EU'])
print( d.values() ) #Output: dict_values([200, 150, 2])
```

## Week 4: NumPy

* [Part 1 of Week 4 Assignment -Basic NumPy Exercises](https://github.com/hsarfraz/Oxford-Python-pt-1-2/blob/main/1.4_week4_pt1_assignment.ipynb)
* [Part 2 of Week 4 Assignment -Working with datasets using Numpy](https://github.com/hsarfraz/Oxford-Python-pt-1-2/blob/main/1.4_week4_pt2_assignment.ipynb)

List vs. Arrays
* Lists and Arrays in Python do use the subscript operator `[]` ro refer to specific elements
* Elements in both, a array and list, are indexed
* Lists in Python are resizeable, unlike static arrays which are fixed
* Python lists can store elements of different types, whereas arrays are declared to store values of one type
* Fixed-size arrays need to have the number of elements defined before hand, whereas flexible sized array collections don't need to have a pre-defined number of elements

Overview of Numpy
* Numerical Python (NumPy) is a package full of methods that can be used to perform useful operations on data
* NumPy provides a convenient API (Application Programmable Interface) that provides a way to 'interface' with/operate on data
* It is a more efficient way to search/sort/store data than the "loosely" typed nature of Python that we have seen so far.

Casting/Up-Casting a NumPy array
* Up-Casting is when you convert a variable from one data type to another
```
import numpy as np #this line will apply for the other code blocks as well
a = np.array([1,2,3], dtype = 'float32')
a
#Output: array([1.,2.,3.,4.], dtype=float32)
```

NumPy arrange
```
a = mp.arrange(10)
a
#Output: array([0,1,2,3,4,5,6,7,8,9])
```

Multi-Dimensional NumPy Array
* note how the dimensionality of the array is passed as a tuple
```
a = np.ones((3,2))
a
#OuputL array([[1.,1.],
#              [1.,1.],
#              [1.,1.]])
  ```

Eye NumPy Method (used for correlations)
```
a = np.eye(2)
a
# Output: array([[1.,0.],
#                [0., 1.]])
```

2D NumPy array
```
a = np.random.randint(8, size=(2,2))
a
#Output: array([[5, 3],
#               [0, 7])
```

Array Attributes
```
a = np.random.randint(9, size=(3,3))
print('size', a.size)
print('shape', a.shape)
print('dimensions', a.ndim)
#Output: size: 9
#        shape: (3,3)
#        dimensions: 2
```

Array Indexing
* This is how indexing works for array elements `x[start:stop:step]`
* If left unspecified, the default values for the index are:
 * `start=0`
 *  `stop=size of dimension`
 *  `step=1`

Vectorization
```
a = np.array([1,2,3])
b = np.array([4,5,6])
c = np.sum(a * b)
print(c)
# Output: 32 = (1*4) + (2*5) + (3*6)
```

Boolean Masking
```
a = np.array([[1,2,3], [4,5,6], [7,8,9]])
b = np.array([10,20,30])
c = a + b
mask = (c > 20)
mask
# Output: array([[False, True, True],
#                [False, True, True],
#                [False, True, True]])

c[mask]
#Output: array([22,33,25,36,28,39]) - only returns the TRUE values
```
## Week 5: Pandas for data science I 

* [Week 5 Assignment](https://github.com/hsarfraz/Oxford-Python-pt-1-2/blob/main/1.5_week5_assignment.ipynb)

Pandas
* Pandas is a package that supplies data analysis tools in python
* Dataframes provide convenient formatiing to visualise the data source. CSV files and NumPy arrays are used as a source for these dataframes (GroupBy)
* It provides useful functions from summaries and descriptive statisitcs of data, in addition to SQL joins

Pandas Series
* A series can be converted to a Pandas Dataframe (often used for timeseries analysis which will be explored later)

Creating a Series 
```
labels = ['a','b','c']
my_list = [10,20,30]
pd.Series(data=my_list,index=labels)

# Output: a 10
#         b 20
#         c 30
# dtype: int64
```

How to get the total na values in a DataFrame
```
df.isna().sum()
```

Using groupby on a DataFrame
```
df.groupby('salary').mean()

# Output: salary age
#         50000  25
```

Reading CSV values and converting it to a Dataframe
```
import os #for establishing working directory
os. getcwd() #getting current working directory
path = 'C:/work/Mod 1/my_dir'
os. chdir(path) #path would be the new working directory

data = pd.read_csv('dataset.csv')
df = pd.DataFrame(data)
type(df)
```

## Week 6: Pandas for data science II

* [Tutorial of Concatenations and Joins of Pandas Data Frames](https://github.com/hsarfraz/Oxford-Python-pt-1-2/blob/main/1.6_week6_Concatenations%20and%20Joins%20of%20Pandas%20Data%20Frames.ipynb)
   * This tuorial uses `pd.concat()` and `pd.merge()` to show how the joining of two separate Pandas Dataframes work
   * `pd.merge()` can be used to specify a specific type of join (such are inner, outer, left, or right)
   *   `pd.concat()` can be used to stack two dataframes on top of each other (vertical stack)
   * `pd.DataFrame.append()` stacks the dataframes vertically
   * `pd.DataFrame.join()` joins based on the indexes

* [Tutorial on how to use the `map()`, `filter()`, and `functools.reduce()` functions](https://github.com/hsarfraz/Oxford-Python-pt-1-2/blob/main/1.6_week6_map%20filter%20and%20reduce%20functions.ipynb)
  * `map(func, iterable)` applies the function 'func' evenly to all the items in the 'iterable' object
  * `filter(func, iterable)` takes in 'func' as a boolean condition. All the items in 'iterable' for which 'func' returns False are filtered out
  * `functools.reduce(func, iterable[ ,iterable])` applies a function of two arguments, 'func', cumulatively to the elements of 'iterable', optionally starting with an initial argument

 Data Manipulation in Python

 * Pandas and Numpy offer vectorized (column-wise operations) ways to perform data manipulation
   * ex. `df['BMI'] = df['Weight (kg)']/df['Height (cm)']/100)**2` would go through each row in the 'weight' and 'height' column without the need to use a for-loop

Quantitative Variables (Discrete & Continuous) and Categorical Variables (Ordinal & Nominal)
<img src="image/variable types.jpg" width="700">


Correlation Coefficient meaning

A correlation coefficient tells us the strength of two or more variables and their direction (positive or negative facing). The graph below illustrates the different types of correlations and the chart below also shows how to interpret each correlation number.
<img src="image/correlation graph illustration.jpg" width="700">
<img src="image/correlation interpretation.jpg" width="700">

## Week 7: Matplotlib for Data visualisation

## Week 8: Object-oriented programming: classes, inheritance, and applications 

## Week 9: Data gathering and cleaning. Text pre-processing for Natural Language Processing (NLP)

NLP Terminology 
* **Corpus**: A collection of documents
* **Token**: A well-defined unit inside a document. It can be a word or a sub-word
* **Vector**: A mathematically convenient representation of a document
* **Model**: An algorithm for transforming vectors from one representation to another

Text pre-processing

Text pre-processing consists of three steps
* **tokenizing** strings and giving an integer id for each possible token (ex. using white spaces and punctuation as token separators)
* some form of **vecorisation** such as:
  * counting the occurrences of tokens in each document
  * normalizing and weighting with diminishing importance tokens that occue in a plurality of samples
  * word embeddings

Tokenization (breaking text into 'tokens')

* Tokenization is the process of breaking down text into smaller meaningful units called tokens
* This crucial step prepares the text for further natural language processing tasks such as part-of-speech tagging and sentiment analysis

```
#imput: "Hey Nick! How are you?"
#tokens = ['Hey', 'Nick', '!', 'How', 'are', 'you', '?']
```

Vectorisation

* Problem: neural network models and statistical methods do not understand strings and characters. Therefore, we would need to convert the strings/characters into numbers so they can be used. This process is called vectorisation
* Vectorisation methods
  * Word Embeddings
  * Bag of Words (BoW)
  * Term Frequencey-Inverse Document Frequency (TF-IDF)
 
 Example of NLP pipeline
 
 <img src="image/example_of_NLP_pipeline.jpg" width="700">

 How to interpret a confusion matrix

 <img src="image/1.9_confusion_matrix.jpg" width="700">

 How to interpret a classification report

1. Precision: Percentage of correct positive predictions relative to total positive predictions.

2. Recall: Percentage of correct positive predictions relative to total actual positives.

3. F1 Score: A weighted harmonic mean of precision and recall. The closer to 1, the better the model.

## Week 10: Introduction to experimental design (timeseries)

# Python Programming for Data Science - Part 2 Syllabus Overview

## Week 1: Introduction to the Course / ML / Linear Regression

## Week 2: Overview of a data-science preprocessing pipeline

## Week 3: Supervised Learning: Regression

## Week 4: Supervised Learning: Classification

## Week 5: More Classification, Decision Trees. Ensemble Methods

## Week 6: Introduction to Neural Networks and Deep Learning

## Week 7: Deep Learning: CNNs for Image Processing and RNNs for Time Series Analysis

## Week 8: Dimensionality Reduction and Unsupervised Learning

## Week 9: RNNs for NLP. Attention-based models (Transformers)

## Week 10: GANs, Autoencoders and Reinforcement Learning
