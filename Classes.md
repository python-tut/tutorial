#Classes and Object Oriented Programming

Classes are an important part of python, it allows us to create objects and manipulate them through methods to reach our goals.

##Creating a class

Creating a class is simple, all it requires is one line of code.
``` python
class Example(object):
```
With our class created it we can begin to input an object.

##Initialize your object

One initialize command will allow you to create you objects.
``` python
def __init__(self, param1, param2, param3):
	self.param1 = param1
	self.param2 = param2
	self.param3 = param3
```
Here `param` is equivalent to any parameters that you wish to add. 

This is how we initialize an object to be manipulated by further methods.

##Scope

Its important to note not all variables may work in your class. This is determined by where the variables are located.
``` python
xkcd = "antigravity"
class Example(object):
	marbles = "marble"
	def __init__(self, param1):
		self.param1 = param1
	def method(self):
		print xkcd
		print marbles
		print self.param1

test = Example("text!")	
test.method()	
```
In this scenario, the variable `xkcd` is outside of the class. It is a global variable and can be used anywhere in the code. On the other hand, the variable `marbles` is declared inside the class. It is a member variable and can only be called inside the class itself. Finally we have `self.param1` which is an instance variable. We can only call it inside of the method because we called `self` as a parameter.

Understanding scope is extremely important and can stop many problems that arise due to improperly called variables.

##Methods

Methods are what makes classes useful. They are the means of manipulating the data we have stored in our class. As seen above methods are similar to functions just called upon our classes. They are limited to only the classes that they reside in so unlike other methods such as `.len()` and `.str()` they will not work on anything that isn't the class they correspond to.

A method is created by:
``` python
def method(self):
	# Rest of the code
```
The method is called by using:
``` python
randomname.method(param)
#param if you have one set otherwise it can be left empty.
```
