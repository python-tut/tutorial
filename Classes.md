#Classes and Object Oriented Programming

Classes are an important part of python, it allows us to create objects and manipulate them through methods to reach our goals.


----------

##Creating a class

Creating a class is simple, all it requires is one line of code.
``` python
class Example(object):
```
With our class created it we can begin to input an object.

----------


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

----------

##Creating your object

Now that we can initialize the object its time to make one. To start we give it a variable.
``` python
class Example(object):
	def __init__(path, params):
		pass
var = Example(params)
```
It is important to note that your variable name will become the `path` so any parameters are entered afterwards.

----------


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


----------


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

Methods can be treated the same way as functions as they perform a very similar function the only main difference being the restrictions on the usage of methods and the way they are implemented. It is important to note that functions can be used on objects, however functions are often less relied on due to their inability to access information locally to the object.


----------


##Inheritance

Classes can be called in the creating of another class to inherit that classes properties, 

``` python
class Example(object):
	def __init___(self):
		# blah blah blah coding blah
	def method(self):
		print "stuff"

class NextExample(Example):
	def post_history(self):
		print "Other Stuff"
```
By calling the previous class in the new class, the new class inherits the objects of the previous class and can thus act on them in a independent environment that will no longer affect other objects in the previous class.

Additionally, a inherited class can override the previous class by naming the method the same as before.

``` python
class Example(object):
	def __init___(self):
		# blah blah blah coding blah
	def method(self):
		print "stuff"

class NextExample(Example):
	def method(self):
		print "OVERRIDE!"
```
Doing so will override the object in the `NextExample` class without affecting objects in the `Example` class. This is useful in ensuring a common method can create different results depending on circumstance.


----------

##Assessment

Create a class and a inherited class and have them print out a different statement for the same method for two different objects.
