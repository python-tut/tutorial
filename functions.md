# Function Syntax and Scope
## Function Basics
Functions in Python are very much like functions in ruby. Here is the basic syntax

``` python
	def hello():
		print "Hello, World!"
	
	hello()
```

If you come from ruby, you'll probably recognize the `def` keyword, which stands for define, followed by the function name. The `def` indicates the start of a function declaration. The name of the function is then followed by parenthesis and a colon. Remember that python uses rigid rules on indents, so anything after the colon that is tabbed will be apart of the function being made. 

For ruby users, notice that the parenthesis are needed, so you cannot leave them off if you are not using them. Also note that there is not `do` and `end` syntax.  Python recognizes the beginning of the function body using the colon and the end using line indents.

##Parameters and Arguments