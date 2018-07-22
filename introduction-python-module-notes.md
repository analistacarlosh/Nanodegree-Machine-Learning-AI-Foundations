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

