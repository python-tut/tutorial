#Control Flow Tutorial



##Conditional Operators

###What is an Operator?

Simple answer can be given using expression 4 + 5 is equal to 9. Here, 4 and 5 are called operands and + is called operator. Python language supports the following types of operators.

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

###Comparison Operators

Assume variable a holds 10 and variable b holds 20, then:

|Operator |Description |Example |
|:------------:|:--------------:|:--------------:|
|==	|Checks if the value of two operands are equal or not, if yes then condition becomes true.|	(a == b) is not true.
|!=|	Checks if the value of two operands are equal or not, if values are not equal then condition becomes true.|	(a != b) is true.
|<>|	Checks if the value of two operands are equal or not, if values are not equal then condition becomes true.|	(a <> b) is true. This is similar to != operator.
|>|	Checks if the value of left operand is greater than the value of right operand, if yes then condition becomes true.	|(a > b) is not true.
|<	|Checks if the value of left operand is less than the value of right operand, if yes then condition becomes true.	|(a < b) is true.
|>=|	Checks if the value of left operand is greater than or equal to the value of right operand, if yes then condition becomes true.|	(a >= b) is not true.
|<=|	Checks if the value of left operand is less than or equal to the value of right operand, if yes then condition becomes true.|	(a <= b) is true.

###Assignment Operators

Assume variable a holds 10 and variable b holds 20, then:

|Operator |Description |Example |
|:------------:|:--------------:|:--------------:|
|=|	Simple assignment operator, Assigns values from right side operands to left side operand|	c = a + b will assigne value of a + b into c
|+=|	Add AND assignment operator, It adds right operand to the left operand and assign the result to left operand|	c += a is equivalent to c = c + a
|-=|	Subtract AND assignment operator, It subtracts right operand from the left operand and assign the result to left operand|	c -= a is equivalent to c = c - a
|*=|	Multiply AND assignment operator, It multiplies right operand with the left operand and assign the result to left operand	|c *= a is equivalent to c = c * a
|/=|	Divide AND assignment operator, It divides left operand with the right operand and assign the result to left operand|	c /= a is equivalent to c = c / a
|%=|	Modulus AND assignment operator, It takes modulus using two operands and assign the result to left operand|	c %= a is equivalent to c = c % a
|**=|	Exponent AND assignment operator, Performs exponential (power) calculation on operators and assign value to the left operand	|c **= a is equivalent to c = c ** a
|//=|	Floor Dividion and assigns a value, Performs floor division on operators and assign value to the left operand	|c //= a is equivalent to c = c // a

###Bitwise Operators

Bitwise operator works on bits and perform bit by bit operation. Assume if a = 60; and b = 13; Now in binary format they will be as follows:

|Operator |Description |Example |
|:------------:|:--------------:|:--------------:|
|& |	Binary AND Operator copies a bit to the result if it exists in both operands. |	(a & b) will give 12 which is 0000 1100
| (pipe) |	Binary OR Operator copies a bit if it exists in eather operand. |	(a "pipe" b) will give 61 which is 0011 1101
|^|	Binary XOR Operator copies the bit if it is set in one operand but not both.|	(a ^ b) will give 49 which is 0011 0001|
|~|	Binary Ones Complement Operator is unary and has the efect of 'flipping' bits.|	(~a ) will give -61 which is 1100 0011 in 2's complement form due to a signed binary number.|
|<<|	Binary Left Shift Operator. The left operands value is moved left by the number of bits specified by the right operand.|	a << 2 will give 240 which is 1111 0000
|>>	|Binary Right Shift Operator. The left operands value is moved right by the number of bits specified by the right operand.|	a >> 2 will give 15 which is 0000 1111|

###Operator Precedence
|Operator |Description |
|:------------:|:--------------:|
|**|	Exponentiation (raise to the power)
|~ + -|	Ccomplement, unary plus and minus (method names for the last two are +@ and -@)
|* / % //|	Multiply, divide, modulo and floor division
|+ -|	Addition and subtraction
|>> <<|	Right and left bitwise shift
|&|	Bitwise 'AND'
|^ (pipe)|	Bitwise exclusive `OR' and regular `OR'
|<= < > >=|	Comparison operators
|<> == !=|	Equality operators
|= %= /= //= -= += *= **=|	Assignment operators
|is is not|	Identity operators
|in not in|	Membership operators
|not or and|	Logical operators

##IF Statement

The **_if_** statement of Python is similar to that of other languages. The if statement contains a logical expression using which data is compared and a decision is made based on the result of the comparison.

Some important pieces of all these statements is that colons and indention are key in Python. You must indent after the colon for it to read the statement. if you do not then it will not be included in the statement. It is as if you are starting a new line or expression.

SYNTAX:
```python
if expression:
  statement(s)
```

EXAMPLE:
```python
var1 = 100
if var1:
   print "1 - Got a true expression value"
   print var1

var2 = 0
if var2:
   print "2 - Got a true expression value"
   print var2
print "Good bye!"
```
RESULT:
```
1 - Got a true expression value
100
Good bye!
```

##IF ELSE Statement

An **_else_** statement can be combined with an if statement. An else statement contains the block of code that executes if the conditional expression in the if statement resolves to 0 or a false value.

The else statement is an optional statement and there could be at most only one else statement following if .


SYNTAX:
```python
if expression:
   statement(s)
else:
   statement(s)
```

EXAMPLE:
```python
var1 = 100
if var1:
   print "1 - Got a true expression value"
   print var1
else:
   print "1 - Got a false expression value"
   print var1

var2 = 0
if var2:
   print "2 - Got a true expression value"
   print var2
else:
   print "2 - Got a false expression value"
   print var2

print "Good bye!"
```

RESULT:
```
1 - Got a true expression value
100
2 - Got a false expression value
0
Good bye!
```

##ELIF

The **_elif_** statement allows you to check multiple expressions for truth value and execute a block of code as soon as one of the conditions evaluates to true.

Like the else, the elif statement is optional. However, unlike else, for which there can be at most one statement, there can be an arbitrary number of elif statements following an if.

SYNTAX:
```python
if expression1:
   statement(s)
elif expression2:
   statement(s)
elif expression3:
   statement(s)
else:
   statement(s)
```

EXAMPLE:
```python
var = 100
if var == 200:
   print "1 - Got a true expression value"
   print var
elif var == 150:
   print "2 - Got a true expression value"
   print var
elif var == 100:
   print "3 - Got a true expression value"
   print var
else:
   print "4 - Got a false expression value"
   print var

print "Good bye!"
```

RESULT:
```
3 - Got a true expression value
100
Good bye!

```



##While Statement

A **_while_** loop statement in Python programming language repeatedly executes a target statement as long as a given condition is true.

SYNTAX:
```python
while expression:
   statement(s)
```

EXAMPLE:
```python
count = 0
while (count < 9):
   print 'The count is:', count
   count = count + 1

print "Good bye!"
```

RESULT:
```
The count is: 0
The count is: 1
The count is: 2
The count is: 3
The count is: 4
The count is: 5
The count is: 6
The count is: 7
The count is: 8
Good bye!
```

##ELSE Statement with WHILE Statement

Python supports to have an else statement associated with a loop statement.

1. If the else statement is used with a for loop, the else statement is executed when the loop has exhausted iterating the list.

2. If the else statement is used with a while loop, the else statement is executed when the condition becomes false.

SYNTAX:
```python
while expression:
  statement(s)
else expression:
  statement(s)
```

EXAMPLE:
```python
count = 0
while count < 5:
   print count, " is  less than 5"
   count = count + 1
else:
   print count, " is not less than 5"
```

RESULT:
```
0 is less than 5
1 is less than 5
2 is less than 5
3 is less than 5
4 is less than 5
5 is not less than 5
```

##FOR Statement

The **_for_** loop in Python has the ability to iterate over the items of any sequence, such as a list or a string.

SYNTAX:
```python
for iterating_var in sequence:
   statements(s)
```

EXAMPLE:
```python
for letter in 'Python':     # First Example
   print 'Current Letter :', letter

fruits = ['banana', 'apple',  'mango']
for fruit in fruits:        # Second Example
   print 'Current fruit :', fruit

print "Good bye!"
```

RESULT:
```
Current Letter : P
Current Letter : y
Current Letter : t
Current Letter : h
Current Letter : o
Current Letter : n
Current fruit : banana
Current fruit : apple
Current fruit : mango
Good bye!
```

You can also iterate through an array. len() is a built in function that is finding the length of the array and the range() is giving the expression a number range to iterate through.

EXAMPLE:
```python
fruits = ['banana', 'apple',  'mango']
for index in range(len(fruits)):
   print 'Current fruit :', fruits[index]

print "Good bye!"
```

RESULT:
```
Current fruit : banana
Current fruit : apple
Current fruit : mango
Good bye!
```




##Assessment

``Create an example that illustrates the combination of``
``an else statement with a for statement that searches``
``for prime numbers from 10 through 20.``
