# tutorial
Standard Data Types:
The data stored in memory can be of many types. For example, a person’s age is stored as a numeric value and his or her address is stored as alphanumeric characters. Python has various standard types that are used to define the operations possible on them and the storage method for each of them.
Python has five standard data types:

1. Numbers
2. String
3. List
4. Tuple
5. Dictionary

Python Numbers:
Number data types store numeric values. They are immutable data types which means that changing the value of a number data type results in a newly allocated object.

Number objects are created when you assign a value to them. For example:

`var1 = 1`
`var2 = 10`
You can also delete the reference to a number object by using the del statement. The syntax of the del statement is:

`del var1[,var2[,var3[….,varN]]]]`
You can delete a single object or multiple objects by using the del statement. For example:

`del var
del var_a, var_b`
Python supports four different numerical types:

1. int (signed integers)

2. long (long integers [can also be represented in octal and       hexadecimal])

3. float (floating point real values)

4. complex (complex numbers)

Examples:
Here are some examples of numbers:

|int   | long           | float     | complex|
|-----:|---------------:|----------:|--------:|
|10    |51924361L       | 0.0       | 3.14j   |
|100   |-0x19323L       |15.20      |45.j     |
|-786  | 0122L          | -21.9     |9.322e-36j|
|080   |0xDEFABCECBDAECB|32.3+e18   | .876j   |
|-0490 |535633629843L   | -90.      |-.6545+0J|
|-0x260 | -052318172735L| -32.54e100| 3e+26J  |
|0x69   |-4721885298529L|70.2-E12   |4.53e-7j

Python allows you to use a lowercase L with long, but it is recommended that you use only an uppercase L to avoid confusion with the number 1. Python displays long integers with an uppercase L.

A complex number consists of an ordered pair of real floating-point numbers denoted by a + bj, where a is the real part and b is the imaginary part of the complex number.

Python Strings:
Strings in Python are identified as a contiguous set of characters in between quotation marks. Python allows for either pairs of single or double quotes. Subsets of strings can be taken using the slice operator ( [ ] and [ : ] ) with indexes starting at 0 in the beginning of the string and working their way from -1 at the end.

The plus ( + ) sign is the string concatenation operator and the asterisk ( * ) is the repetition operator. For example:
```python
!/usr/bin/python

str = ‘Hello World!’

print str # Prints complete string
print str[0] # Prints first character of the string
print str[2:5] # Prints characters starting from 3rd to 5th
print str[2:] # Prints string starting from 3rd character
print str * 2 # Prints string two times
print str + “TEST” # Prints concatenated string
```
This will produce the following result:
```python
Hello World!
H
llo
llo World!
Hello World!Hello World!
Hello World!TEST
```
Python Lists:
Lists are the most versatile of Python’s compound data types. A list contains items separated by commas and enclosed within square brackets ([]). Python doesn't have a native array data structure, but it has the list which is much more general and can be used as a multidimensional array quite easily.

The values stored in a list can be accessed using the slice operator ( [ ] and [ : ] ) with indexes starting at 0 in the beginning of the list and working their way to end -1. The plus ( + ) sign is the list concatenation operator, and the asterisk ( * ) is the repetition operator. For example:

!/usr/bin/python
```python
list = [ ‘abcd’, 786 , 2.23, ‘john’, 70.2 ]
tinylist = [123, ‘john’]

print list # Prints complete list
print list[0] # Prints first element of the list
print list[1:3] # Prints elements starting from 2nd till 3rd
print list[2:] # Prints elements starting from 3rd element
print tinylist * 2 # Prints list two times
print list + tinylist # Prints concatenated lists
This will produce the following result:

[‘abcd’, 786, 2.23, ‘john’, 70.200000000000003]
abcd
[786, 2.23]
[2.23, ‘john’, 70.200000000000003]
[123, ‘john’, 123, ‘john’]
[‘abcd’, 786, 2.23, ‘john’, 70.200000000000003, 123, ‘john’]
```
Python Tuples:
A tuple is another sequence data type that is similar to the list. A tuple consists of a number of values separated by commas. Unlike lists, however, tuples are enclosed within parentheses.

The main differences between lists and tuples are: Lists are enclosed in brackets ( [ ] ) and their elements and size can be changed, while tuples are enclosed in parentheses ( ( ) ) and cannot be updated. Tuples can be thought of as read-only lists. For example:

!/usr/bin/python
```python
tuple = ( ‘abcd’, 786 , 2.23, ‘john’, 70.2 )
tinytuple = (123, ‘john’)

print tuple # Prints complete list
print tuple[0] # Prints first element of the list
print tuple[1:3] # Prints elements starting from 2nd till 3rd
print tuple[2:] # Prints elements starting from 3rd element
print tinytuple * 2 # Prints list two times
print tuple + tinytuple # Prints concatenated lists
This will produce the following result:

(‘abcd’, 786, 2.23, ‘john’, 70.200000000000003)
abcd
(786, 2.23)
(2.23, ‘john’, 70.200000000000003)
(123, ‘john’, 123, ‘john’)
(‘abcd’, 786, 2.23, ‘john’, 70.200000000000003, 123, ‘john’)
```
Following is invalid with tuple, because we attempted to update a tuple, which is not allowed. Similar case is possible with lists:

!/usr/bin/python
```python
tuple = ( ‘abcd’, 786 , 2.23, ‘john’, 70.2 )
list = [ ‘abcd’, 786 , 2.23, ‘john’, 70.2 ]
tuple[2] = 1000 # Invalid syntax with tuple
list[2] = 1000 # Valid syntax with list
```
Python Dictionary:
Python’s dictionaries are kind of hash table type. They work like associative arrays or hashes found in Perl and consist of key-value pairs. A dictionary key can be almost any Python type, but are usually numbers or strings. Values, on the other hand, can be any arbitrary Python object.

Dictionaries are enclosed by curly braces ( { } ) and values can be assigned and accessed using square braces ( [] ). For example:

!/usr/bin/python
```python
dict = {}
  dict[‘one’] = “This is one”
  dict[2] = “This is two”

  tinydict = {‘name’: ‘john’,’code’:6734, ‘dept’: ‘sales’}

  print dict[‘one’] # Prints value for ‘one’ key
  print dict[2] # Prints value for 2 key
  print tinydict # Prints complete dictionary
  print tinydict.keys() # Prints all the keys
  print tinydict.values() # Prints all the values
  ```
  This will produce the following result:

  This is one
  This is two
  ```python
  {‘dept’: ‘sales’, ‘code’: 6734, ‘name’: ‘john’}
  [‘dept’, ‘code’, ‘name’]
  [‘sales’, 6734, ‘john’]
  ```
  Dictionaries have no concept of order among elements. It is incorrect to say that the elements are “out of order”; they are simply unordered.

  Data Type Conversion:
  Sometimes, you may need to perform conversions between the built-in types. To convert between types, you simply use the type name as a function.

  There are several built-in functions to perform conversion from one data type to another. These functions return a new object representing the converted value.
 a long integer. base specifies the base if x is a string.

Data manipulation
  string methods
  len()
  lower()
  upper()
  str()
  str(x)
  List Method
  list
  list.append(x)
  Add an item to the end of the list; equivalent to    a[len(a):] = [x].
  list.extend(L)
  list.insert(i, x)
  list.remove(x)
  list.pop([i])
  list.index(x)
  list.count(x)
  list.sort(cmp=None, key=None, reverse=False)
 list.reverse()


  An example that uses most of the list methods:
  ```python
  >>>
  >>> a = [66.25, 333, 333, 1, 1234.5]
  >>> print a.count(333), a.count(66.25), a.count('x')
  2 1 0
  >>> a.insert(2, -1)
  >>> a.append(333)
  >>> a
  [66.25, 333, -1, 333, 1, 1234.5, 333]
  >>> a.index(333)
  1
  >>> a.remove(333)
  >>> a
  [66.25, -1, 333, 1, 1234.5, 333]
  >>> a.reverse()
  >>> a
  [333, 1234.5, 1, 333, -1, 66.25]
  >>> a.sort()
  >>> a
  [-1, 1, 66.25, 333, 333, 1234.5]
  >>> a.pop()
  1234.5
  >>> a
  [-1, 1, 66.25, 333, 333]
  ```python
