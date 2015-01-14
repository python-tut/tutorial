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

An else statement can be combined with an if statement. An else statement contains the block of code that executes if the conditional expression in the if statement resolves to 0 or a false value.

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


##While Statement

SYNTAX:
```python

```

EXAMPLE:
```python

```

RESULT:
```

```




##FOR Statement

SYNTAX:
```python

```

EXAMPLE:
```python

```

RESULT:
```

```





##Assessment
