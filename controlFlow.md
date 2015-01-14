#Control Flow Tutorial



##conditional Operators

###What is an Operator?

###Math Operators
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

##IF ELSE
```python
if x
```





##While






##FOR







##Assessment
