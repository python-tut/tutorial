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

For ruby users, notice that the parenthesis are needed, so you cannot leave them off if you are not using them. Also note that there is not `do` and `end` syntax.  Python recognizes the beginning of the function body using the colon and the end using line indents.

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

## Scope