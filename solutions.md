#SOLUTIONS





##Control Flow Assessment Solution:

```python
for num in range(10,20):  #to iterate between 10 to 20
   for i in range(2,num): #to iterate on the factors of the number
      if num%i == 0:      #to determine the first factor
         j=num/i          #to calculate the second factor
         print '%d equals %d * %d' % (num,i,j)
         break #to move to the next number, the #first FOR
   else:                  # else part of the loop
      print num, 'is a prime number'
```

Which should output:
```
10 equals 2 * 5
11 is a prime number
12 equals 2 * 6
13 is a prime number
14 equals 2 * 7
15 equals 3 * 5
16 equals 2 * 8
17 is a prime number
18 equals 2 * 9
19 is a prime number
```

##Functions Assessment Solution:
1.
``` python
	import random

	def sample(list):
		return list[random.randrange(0,len(list))]

	print sample([1,2,3,4,5])
```
2.
```python
	import random

	def sample(list):
		return list[random.randrange(0,len(list))]

	def sampleList():
		list = [1,2,3,4,5]
		return sample(list)

	print sampleList()
```

##Classes assignment:
``` python
class Example(object):
	def __init__(path, name):
		path.name = path
	def method(path):
		print "Answer 1"

class BetterExample(Example):
	def method(path):
		print "Answer 2"

obj1 = Example("Object 1")
obj2 = BetterExample("Object 2")

obj1.method()
obj2.method()
```
