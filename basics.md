# Basic Syntax
Hey! Now we'll be going over the basic syntax you'll need to use Python. To make this a bit easier, we'll provide the Javascript equivalent as well.

## Variable Declaration
Python is completely object oriented. You do not need to declare variables before using them, or to declare their type. Every variable in Python is an object, thankfully. Also python interprets and declares variable for you when you set them equal to a value.

This section will go over a few basic types of variables: Numbers &  Strings.

###Math Operators
Assume variable a holds 10 and variable b holds 20, then:

|Operator |Description |Example |
|:------------:|:--------------:|:--------------:|
|+|	Addition - Adds values on either side of the operator	|a + b will give 30
|-|	Subtraction - Subtracts right hand operand from left hand operand|	a - b will give -10
|* |	Multiplication - Multiplies values on either side of the operator	|a * b will give 200
|/|	Division - Divides left hand operand by right hand operand|	b / a will give 2
|%|	Modulus - Divides left hand operand by right hand operand and returns remainder	|b % a will give 0
|**|	Exponent - Performs exponential (power) calculation on operators|	a**b will give 10 to the power 20
|//|	Floor Division - The division of operands where the result is the quotient in which the digits after the decimal point are removed.|	9//2 is equal to 4 and 9.0//2.0 is equal to 4.0


### Numbers
To define an integer, use the following syntax:

- myint = 7

### Strings
Strings are defined either with a single quote or a double quotes. Example:
 - mystring = 'hello'
 - mystring = "bye"

Here are a few examples:
  - pen = 10
  - pen_in_a_desk = 3
  - students = 5

You get the point. Also, variables can not be numbers. So 7 = var, isn't valid.

Also an easier way to remember this is variables appear on the left of the equal sign and values appear on the right side.

## Printing
You'll use print() a whole lot in the future. All it does is output whatever is inside the parentheses.

Print is a function that we will go into later, but just understand that it can take a value. On the first line, we provide a string value "My first Python code!", which is a string because of the quotes. So, you just told Python to output that string to the console. Python completes that task and moves onto the next line where it prints out a different string.

Using the variables from the last section, you'll learn how to print strings:

- print(pen)
- print(pen_in_a_desk)
- print(students)

## Comments

To make a multiline comment type " ''' ".  
If you're using a text editor, make comments by entering '#' before the line of code. To comment multiple lines of code highlight the lines hold CTRL then press the '/' code.

## Excercises

1. Write a program that asks the user to type in a string, and then tells the user how long that string was.
