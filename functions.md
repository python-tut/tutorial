# Function Syntax and Scope

Functions are extremely powerful and essential to any useful code. It's easiest to think of functions in python like functions in math. They are first called, usually taking in some values, form operation 

## Function Basics

Functions in Python are very much like functions in ruby. Here is the basic syntax

``` python
	def hello():
		print "Hello, World!"
	
	hello()
```

If you come from ruby, you'll probably recognize the `def` keyword, which stands for define, followed by the function name. The `def` indicates the start of a function declaration. The name of the function is then followed by parenthesis and a colon. Remember that python uses rigid rules on indents, so anything after the colon that is tabbed will be apart of the function being made. 

For ruby users, notice that the parenthesis are needed, so you cannot leave them off if you are not using them. Also note that there is no `do` and `end` syntax.  Python recognizes the beginning of the function body using the colon and the end using line indents.

In order to use the function, you must call the function. This is represented by simply entering in the name of the function with parenthesis: `hello()`.

##Parameters and Arguments

Functions wouldn't be all that useful unless your able to pass things to them. Heres is what this concepts look like

``` python
	def printStr(str):
		print str;
	
	printStr("Hello, World!")
```
First lets discuss the terms. An argument is what is passed into the function. In this case, that would be `"Hello, World!"`. While a parameter is the variable that is declared with the function. In this case, that would be `str`. 

This syntax is exactly like most other languages, including ruby.

##Returning 
All the function we have been using is doing so far is printing a string. Most of the time, this is not very useful. A function in mathematics takes arguments, does some operation, and then returns a new value. Now lets look at how we return values python.

``` python
	def add(num1,num2):
		return num1 + num2
	
	print add(1,2)
```
Notice that the print statement is no longer in the function, but instead is called on the function call itself. This is because the function is returning the value, not printing it. You can think about it as the function call is being replaced with the value that is being returned, in which we are then printing to the terminal.

This is very similar to the return statement in both JavaScript and Ruby and probably most other languages.

##Functions in Functions so your function can function

One thing to note about Python is that is allows you to call functions within functions. 

``` python
	def add():
		return addMore()
	def addMore():
		return 1
	print add()
```
`addMore()`is called within the other function `add()`. If you come from JS or Ruby, this is very familiar. 

## Scope

Scope is a difficult and abstract concept for a lot of people to understand. Python has strict scoping  guidelines that can be broken into two different rules. When looking for a variable name, python essentially looks in two places.

1. The local namespace, or scope.
2. The global scope.

The local scope is any variable that is declared within the given function. The global scope is any variable that is declared outside of any function or class. It always does it in this order, so the local variable will always be used over the global variable.

Lets do some examples

``` python
	n = 1
	def add():
		return n + 1
	print add()
```
This code will not break the program. Python first checks for `n` in the local function, which it can't find, and then looks for it in the global scope, where it is declared.
``` python
	def add():
		n = 1
		return n + 1
	print add()
	print n
```
This code will break the program. The last line, `print(n)`, looks for n in the local scope, which is the global scope, and the global scope, which is the same as before, and cannot find the variable declaration. In short, any variable declared within a function or loop is immediately "destroyed" one the function or loop ends. 

One more example that is important is that the local scope only specifies the current function's scope, and not any "outer" scopes that may be in play. Lets look at a slightly different example from above:
``` python
	def add():
		n = 1
		return addMore()
	def addMore():
		return n + 1
	print add()
```
Intuitively, this program looks like it would work. Since the `addMore()` function is called in the `add()` function, you would think that `n` could be used. This is, in fact, false. The local scope only includes what is in the current function, and not in any function that it may be nested in.

##Quirks
One thing to be careful of when your sending in arguments into a function is that you can change them with mutator methods. For example, appending an element onto a list.
``` python
	arr = [1,2]
	def change(array):
		array.append(3)
		print array
	change(arr)
	print arr
```
In this function, a list is sent in as a argument, and the related parameter is appended to. The original `arr` is changed to `[1,2,3]`, even outside of the function. 

Another thing to note is when you assign a variable name in a function, it overides the global variable while inside that function.

``` python
	num = 2
	def change():
		num = 3
		print num
	change()
	print num
```
Inside the function, `num` is 3 and outside `num` is still 2. The function created a local variable called `num`. 

One last thing to note is that Python will create the local variable before is reads what it is being assigned to. From the last example, this will throw an error.

``` python
	num = 2
	def change():
		num = num + 3
		print num
	change()
	print num
```
The functions initializes the local variable `num` and before assigning it anything tries to assign it itself. It causes an error. To fix this, all you do is have to add a buffer variable.

``` python
	num = 2
	def change():
		num_alt = num
		num = num_alt + 3
		print num
	change()
	print num
```
This will work fine. 


##Built-in Functions
Python has a plethora of built-in functions that it allows you to use. To use them, its as simple as calling a function that you made yourself. Here is an example:
``` python
	print abs(-42)
```
`abs()` is a built-in python function that returns the absolute value of the given number. As expected, this program would print `42`. 

Here is just a few of the many Python built-in functions
* `abs()`
* `min()`
* `max()`
* `any()`
* `filter()`
* `map()`

##Importing Functions

Ever wonder where all of the built-in functions are coming from? They're essentially coming from files that declare python functions the same way we did above. You can actually make your own functions and import them into other documents to use functions you write. This is how libraries are created and used. For example, Python has a math module (or library) that we can use. We need to, however, import it first.

``` python
	import math 
	
	print math.sqrt(16)
```
`math` is the name the module that you are importing, or the name of the file that you want to use methods from. When using one of these methods, you then have to write `module.function()` in order to use them. Math has a variety of very useful functions that you will undoubtedly need if you keep working with python.

This is very similar to Ruby's `require` keyword.

## Putting it All Together 

1. Create a function that takes in a list and returns a random item from that list (hint: look up the random module)
2. Create a function with a hard-coded list that calls the function above and returns a random item from the local hard-coded list.