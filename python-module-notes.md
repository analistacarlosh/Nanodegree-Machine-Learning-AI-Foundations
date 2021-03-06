# Notes of Python language in Machine Learning Introduction Course

## Standard of Python
https://www.python.org/dev/peps/pep-0008/

## Logical operators;

`and == && and or == ||`

### String
is umutable;
concat `print("C" + "A")`
`len("string") # return the count of characteres of a string`
`print(type("carlos"))`

`print("hippo"*12)`
`hippohippohippohippohippohippohippohippohippohippohippohippo`

**print a string and integer**
`print("This week's total sales: {total_sales} ".format(total_sales=total_sales))`

**String Methods**
In this video you were introduced to methods. Methods are like some of the functions you have already seen:

`len("this")`
`type(12)`
`print("Hello world")`
These three above are functions - notice they use parentheses, and accept one or more arguments. Functions will be studied in much more detail in a later lesson!

A method in Python behaves similarly to a function. Methods actually are functions that are called using dot notation. For example, lower() is a string method that can be used like this, on a string called "sample string": sample_string.lower().

### List (array)
You saw here that you can create a list with square brackets. Lists can contain any mix and match of the data types you have seen so far.

`list_of_random_things = [1, 3.4, 'a string', True]`

**Slice and Dice with Lists**
You saw that we can pull more than one value from a list at a time by using slicing. When using slicing, it is important to remember that the lower index is inclusive and the upper index is exclusive.

Therefore, this:

```
>>> list_of_random_things = [1, 3.4, 'a string', True]
>>> list_of_random_things[1:2]
[3.4]
```
**Are you in OR not in?**
You saw that we can also use in and not in to return a bool of whether an element exists within our list, or if one string is a substring of another.

>>> 'this' in 'this is a string'
True
>>> 'in' in 'this is a string'
True
>>> 'isa' in 'this is a string'
False
>>> 5 not in [1, 2, 3, 4, 6]
True
>>> 5 in [1, 2, 3, 4, 6]
False

Quiz: Slicing Lists
Select the three most recent dates from this list using list slicing notation. Hint: negative indexes work in slices!

eclipse_dates = ['June 21, 2001', 'December 4, 2002', 'November 23, 2003',
                 'March 29, 2006', 'August 1, 2008', 'July 22, 2009',
                 'July 11, 2010', 'November 13, 2012', 'March 20, 2015',
                 'March 9, 2016']
                 
                 
# TODO: Modify this line so it prints the last three elements of the list
print(eclipse_dates[-3:])


**Useful Functions for Lists I
len() returns how many elements are in a list.
max() returns the greatest element of the list. How the greatest element is determined depends on what type objects are in the list. The maximum element in a list of numbers is the largest number. The maximum elements in a list of strings is element that would occur last if the list were sorted alphabetically. This works because the the max function is defined in terms of the greater than comparison operator. The max function is undefined for lists that contain elements from different, incomparable types.
min() returns the smallest element in a list. min is the opposite of max, which returns the largest element in a list.
sorted() returns a copy of a list in order from smallest to largest, leaving the list unchanged.

**
len, max, min

**
sorted, join, and Lists

**
append and Lists


**Tuples
A tuple is another useful container. It's a data type for immutable ordered sequences of elements. They are often used to store related pieces of information. Consider this example involving latitude and longitude:

location = (13.4125, 103.866667)
print("Latitude:", location[0])
print("Longitude:", location[1])
Tuples are similar to lists in that they store an ordered collection of objects which can be accessed by their indices. Unlike lists, however, tuples are immutable - you can't add and remove items from tuples, or sort them in place.

Tuples can also be used to assign multiple variables in a compact way.

dimensions = 52, 40, 100
length, width, height = dimensions
print("The dimensions are {} x {} x {}".format(length, width, height))
The parentheses are optional when defining tuples, and programmers frequently omit them if parentheses don't clarify the code.

In the second line, three variables are assigned from the content of the tuple dimensions. This is called tuple unpacking. You can use tuple unpacking to assign the information from a tuple into multiple variables without having to access them one by one and make multiple assignment statements.

If we won't need to use dimensions directly, we could shorten those two lines of code into a single line that assigns three variables in one go!

length, width, height = 52, 40, 100
print("The dimensions are {} x {} x {}".format(length, width, height))

***Sets
A set is a data type for mutable unordered collections of unique elements. One application of a set is to quickly remove duplicates from a list.

numbers = [1, 2, 6, 3, 1, 1, 6]
unique_nums = set(numbers)
print(unique_nums)
This would output:

{1, 2, 3, 6}
Sets support the in operator the same as lists do. You can add elements to sets using the add method, and remove elements using the pop method, similar to lists. Although, when you pop an element from a set, a random element is removed. Remember that sets, unlike lists, are unordered so there is no "last element".

fruit = {"apple", "banana", "orange", "grapefruit"}  # define a set

print("watermelon" in fruit)  # check for element

fruit.add("watermelon")  # add an element
print(fruit)

print(fruit.pop())  # remove a random element
print(fruit)

When you pop an element from a set a random element is removed (remember that sets, unlike lists, are unordered so there is no "last element"). The number 5 may or may not be removed.

***Dictionaries And Identity Operators
Dictionaries
A dictionary is a mutable data type that stores mappings of unique keys to values. Here's a dictionary that stores elements and their atomic numbers.

elements = {"hydrogen": 1, "helium": 2, "carbon": 6}
Dictionaries can have keys of any immutable type, like integers or tuples, not just strings. It's not even necessary for every key to have the same type! We can look up values or insert new values in the dictionary using square brackets that enclose the key.

**Compound Data Structures
We can include containers in other containers to create compound data structures. For example, this dictionary maps keys to values that are also dictionaries!

elements = {"hydrogen": {"number": 1,
                         "weight": 1.00794,
                         "symbol": "H"},
              "helium": {"number": 2,
                         "weight": 4.002602,
                         "symbol": "He"}}

### Data types            
** Int, string, bool, double, List, Tuples, Sets, Dictionary **

## Control flow lesson

### If Statement

``` if phone_balance < 5:
    phone_balance += 10
    bank_balance -= 10
```

### If, Elif, Else

``` if season == 'spring':
    print('plant the garden!')
elif season == 'summer':
    print('water the garden!')
elif season == 'fall':
    print('harvest the garden!')
elif season == 'winter':
    print('stay indoors!')
else:
    print('unrecognized season')
```

### Indentation

**Spaces or Tabs?**
The Python Style Guide recommends using 4 spaces to indent, rather than using a tab. Whichever you use, be aware that "Python 3 disallows mixing the use of tabs and spaces for indentation."

### For Loops
Python has two kinds of loops - for loops and while loops. A for loop is used to "iterate", or do something repeatedly, over an iterable.

An iterable is an object that can return one of its elements at a time. This can include sequence types, such as strings, lists, and tuples, as well as non-sequence types, such as dictionaries and files.

**Example**
Let's break down the components of a for loop, using this example with the list cities:

```
names = ["Joey Tribbiani", "Monica Geller", "Chandler Bing", "Phoebe Buffay"]
usernames = []

# write your for loop here
for name in names:
    usernames.append(name.lower().replace(" ", "_"))
    
print(usernames)
```

**for and rand()**
```
usernames = ["Joey Tribbiani", "Monica Geller", "Chandler Bing", "Phoebe Buffay"]

for i in range(len(usernames)):
    usernames[i] = usernames[i].lower().replace(" ", "_")

print(usernames)
```

**Iterating Through Dictionaries with For Loops**

```
for key, value in cast.items():
    print("Actor: {}    Role: {}".format(key, value))
```

**While Loops**
```
card_deck = [4, 11, 8, 5, 13, 2, 8, 10]
hand = []

# adds the last element of the card_deck list to the hand list
# until the values in hand add up to 17 or more
while sum(hand)  < 17:
    hand.append(card_deck.pop())Bom d
```

## Functions lesson

**Defining Functions**
Example of a function definition:
```
def cylinder_volume(height, radius):
    pi = 3.14159
    return height * pi * radius ** 2
```

**Default Arguments**
```
def cylinder_volume(height, radius=5):
    pi = 3.14159
    return height * pi * radius ** 2
```

**Quiz: readable_timedelta**
```
def readable_timedelta(days):
    week = days // 7
    days = days % 7
    return "{} week(s) and {} days(s).".format(week,days)

print(readable_timedelta(6))
```

### Docstrings

```
def population_density(population, land_area):
    """Calculate the population density of an area.

    Parameters:
    population: int. The population of that area
    land_area: int or float. This function is unit-agnostic, if you pass in values in terms
    of square km or square miles the function will return a density in those units.

    Returns: 
    population_density: population / land_area. The population density of a particular area.
    """
    return population / land_area
```

### Lambda Expressions
You can use lambda expressions to create anonymous functions. That is, functions that don’t have a name.

**With a lambda expression, this function:**
```
def multiply(x, y):
    return x * y
```
**can be reduced to:**
`multiply = lambda x, y: x * y`

**Both of these functions are used in the same way. In either case, we can call multiply like this:**
`multiply(4, 7)`

**Lambda with Map**
```
numbers = [
              [34, 63, 88, 71, 29],
              [90, 78, 51, 27, 45],
              [63, 37, 85, 46, 22],
              [51, 22, 34, 11, 18]
           ]

averages = list(map(lambda x: sum(x) / len(x), numbers))
print(averages)
```

**Lambda with Filter**
```
cities = ["New York City", "Los Angeles", "Chicago", "Mountain View", "Denver", "Boston"]

short_cities = list(filter(lambda x: len(x) < 10, cities))
print(short_cities)
```
## Scripts lesson

**Install Python Using Anaconda**

**Scripting With Raw Input**

**input function**
```
name = input("Enter your name: ")
print("Hello there, {}!".format(name.title()))
```

```
num = int(input("Enter an integer"))
print("hello" * num)
```

**eval function**
```
result = eval(input("Enter an expression: "))
print(result)
```

**Generate Messages**
```
names = input("Enter names separated by commas: ").title().split(",")
assignments = input("Enter assignment counts separated by commas: ").split(",")
grades = input("Enter grades separated by commas: ").split(",")

message = "Hi {},\n\nThis is a reminder that you have {} assignments left to \
submit before you can graduate. You're current grade is {} and can increase \
to {} if you submit all assignments before the due date.\n\n"

for name, assignment, grade in zip(names, assignments, grades):
    print(message.format(name, assignment, grade, int(grade) + int(assignment)*2))
```

### Try Statement
We can use try statements to handle exceptions.

```
try:
    # some code
except ValueError:
    # some code
```

```
try:
    # some code
except ValueError, KeyboardInterrupt:
    # some code
```

```
try:
    # some code
except Exception as e:
   # some code
   print("Exception occurred: {}".format(e))
```

### Reading a File
```
f = open('my_path/my_file.txt', 'r')
file_data = f.read()
f.close()
```

### Writing to a File
```
f = open('my_path/my_file.txt', 'w')
f.write("Hello there!")
f.close()
```

### With
Python provides a special syntax that auto-closes a file for you once you're finished using it.

```
with open('my_path/my_file.txt', 'r') as f:
    file_data = f.read()
```

```
def create_cast_list(filename):
    cast_list = []
    #use with to open the file filename
    #use the for loop syntax to process each line
    #and add the actor name to cast_list

    return cast_list

cast_list = create_cast_list('flying_circus_cast.txt')
for actor in cast_list:
    print(actor)
```

### Importing Local Scripts

`import useful_functions`

```
import useful_functions as uf
uf.add_five([1, 2, 3, 4])
```

### Using a main block

```
# demo.py

import useful_functions as uf

scores = [88, 92, 79, 93, 85]

mean = uf.mean(scores)
curved = uf.add_five(scores)

mean_c = uf.mean(curved)

print("Scores:", scores)
print("Original Mean:", mean, " New Mean:", mean_c)

print(__name__)
print(uf.__name__)
```

```
# useful_functions.py

def mean(num_list):
    return sum(num_list) / len(num_list)

def add_five(num_list):
    return [n + 5 for n in num_list]

def main():
    print("Testing mean function")
    n_list = [34, 44, 23, 46, 12, 24]
    correct_mean = 30.5
    assert(mean(n_list) == correct_mean)

    print("Testing add_five function")
    correct_list = [39, 49, 28, 51, 17, 29]
    assert(add_five(n_list) == correct_list)

    print("All tests passed!")

if __name__ == '__main__':
    main()
```

### The Python Standard Library
https://docs.python.org/3/library/

### Quiz: Password Generator
Write a function called generate_password that selects three random words from the list of words word_list and concatenates them into a single string. Your function should not accept any arguments and should reference the global variable word_list to build the password.

```
# Use an import statement at the top
import random

word_file = "words.txt"
word_list = []

#fill up the word_list
with open(word_file,'r') as words:
	for line in words:
		# remove white space and make everything lowercase
		word = line.strip().lower()
		# don't include words that are too long or too short
		if 3 < len(word) < 8:
			word_list.append(word)

# Add your function generate_password here
# It should return a string consisting of three random words 
# concatenated together without spaces
def generate_password():
    randomWord = ""
    for i in range(3):
        randomWord += random.choice(word_list)
    return randomWord

# test your function
print(generate_password())
```

**Which Module?**
**Which module can tell you the current time and date?**
`8.1. datetime — Basic date and time types`

**Which module has a method for changing the current working directory?**
`11.2. os.path`

**Which module can read data from a comma separated values (.csv) file into Python dictionaries for each row?**
`14.1. csv — CSV File Reading and Writing`

**Which module can help extract all of the files from a zip file?**
`13.5. zipfile`

**Which module can say how long your code took to run?**
`30. Python Runtime Services`
https://docs.python.org/3/library/timeit.html
https://docs.python.org/3/library/profile.html


### Techniques for Importing Modules

To import multiple individual objects from a module:
`from module_name import first_object, second_object`

To import an object from a module and rename it:
`from module_name import object_name as new_name`

Import all submodules from module
`import module_name`

**Modules, Packages, and Names**
`import package_name.submodule_name`

### Third-Party Libraries
Package manager is pip
`pip install package_name`

**Using a requirements.txt File**

```
beautifulsoup4==4.5.1
bs4==0.0.1
pytz==2016.7
requests==2.11.1
```

You can use pip to install all of a project's dependencies at once by typing `pip install -r requirements.txt` in your command line.

**Useful Third-Party Packages**

* IPython - A better interactive Python interpreter
* requests - Provides easy to use methods to make web requests. Useful for accessing web APIs.
* Flask - a lightweight framework for making web applications and APIs.
* Django - A more featureful framework for making web applications. Django is particularly good for designing complex, content heavy, web applications.
* Beautiful Soup - Used to parse HTML and extract information from it. Great for web scraping.
* pytest - extends Python's builtin assertions and unittest module.
* PyYAML - For reading and writing YAML files.
* NumPy - The fundamental package for scientific computing with Python. It contains among other things a powerful N-dimensional array object and useful linear algebra capabilities.
* pandas - A library containing high-performance, data structures and data analysis tools. In particular, pandas provides dataframes!
* matplotlib - a 2D plotting library which produces publication quality figures in a variety of hardcopy formats and interactive environments.
* ggplot - Another 2D plotting library, based on R's ggplot2 library.
* Pillow - The Python Imaging Library adds image processing capabilities to your Python interpreter.
* pyglet - A cross-platform application framework intended for game development.
* Pygame - A set of Python modules designed for writing games.
* pytz - World Timezone Definitions for Python


Python reference study:

* https://docs.python.org/3/index.html

The websites and blogs of prominent experts
* https://doughellmann.com/blog/ 
* https://eli.thegreenplace.net/