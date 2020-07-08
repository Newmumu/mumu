## Python Examples

### Python Tuples

> Create a tuple
```python
thistuple = ("apple", "banana", "cherry")
print(thistuple)

('apple', 'banana', 'cherry')
```

> Access tuple items
```python
thistuple = ("apple", "banana", "cherry")
print(thistuple[1])

banana
```

> Change tuple values
```python
thistuple = ("apple", "banana", "cherry")
thistuple[1] = "blackcurrant"

# the value is still the same:
print(thistuple)

# 不能修改
('apple', 'banana', 'cherry')
```

> Loop throgh a tuple
```python
thistuple = ("apple", "banana", "cherry")
for x in thistuple:
	print(x)

apple
banana
cherry
```

> Check if a tuple item exists
```python
thistuple = ("apple", "banana", "cherry")
if "apple" in thistuple:
	print("Yes, 'apple' is in the fruits tuple")


Yes, 'apple' is in the fruits tuple
```

> Get the length of tuple
```python
thistuple = ("apple", "banana", "cherry")
print(len(thistuple))

3
```

> Delete a tuple
```python
thistuple = ("apple", "banana", "cherry")
del thistuple
print(thistuple) #this will raise an error because the tuple no longer exists

Traceback (most recent call last):
  File "demo_tuple_del.py", line 3, in <module>
    print(thistuple) #this will raise an error because the tuple no longer exists
NameError: name 'thistuple' is not defined
```

> Using the tuple() constructor to create a tuple
```python
thistuple = tuple(("apple", "banana", "cherry"))
print(thistuple)

('apple', 'banana', 'cherry')
```


### Python Sets

> Create a set
```python
thisset = {"apple", "banana", "cherry"}
print(thisset)

# Note: the set list is unordered, meaning: the items will appear in a random order.
# Refresh this page to see the change in the result.


{'cherry', 'banana', 'apple'}
```

> Loop through a set
```python
thisset = {"apple", "banana", "cherry"}

for x in thisset:
	print(x)


cherry
apple
banana
```

> Check if an item exists
```python
thisset = {"apple", "banana", "cherry"}
print("banana" in thisset)

True
```

> Add an item to a set
```python
thisset = {"apple", "banana", "cherry"}
thisset.add("orange")
print(thisset)

{'cherry', 'orange', 'apple', 'banana'}
```

> Add multiple items to a set
```python
thisset = {"apple", "banana", "cherry"}
thisset.update(["orange", "mango", "grapes"])
print(thisset)

{'grapes', 'orange', 'banana', 'cherry', 'mango', 'apple'}
```

> Get the length of a set
```python
# 可迭代对象，均可使用len()方法进行长度判断
thisset = {"apple", "banana", "cherry"}
print(len(thisset))

3
```

> Remove an item in a set
```python
thisset = {"apple", "banana", "cherry"}
thisset.remove("banana")
print(thisset)

{'cherry', 'apple'}
```

> Remove an item in a set by using the discard() method
```python
thisset = {"apple", "banana", "cherry"}
thisset.discard("banana")
print(thisset)

{'cherry', 'apple'}
```

> Remove the last item in a set by using the pop() method
```python
thisset = {"apple", "banana", "cherry"}
x = thisset.pop()
print(x) #removed item
print(thisset) #the set after removal

banana
{'cherry', 'apple'}
```

> Empty a set
```python
thisset = {"apple", "banana", "cherry"}
thisset.clear()
print(thisset)

set()
```

> Delete a set
```python
thisset = {"apple", "banana", "cherry"}
del thisset
print(thisset) #this will raise an error because the set no longer exists


Traceback (most recent call last):
  File "demo_set_del.py", line 5, in <module>
    print(thisset) #this will raise an error because the set no longer exists
NameError: name 'thisset' is not defined
```

> Using the set() constructor to create a set
```python
thisset = set(("apple", "banana", "cherry"))
print(thisset)
# Note: the set list is unordered, so the result will display the items in a random order.

{'banana', 'apple', 'cherry'}
```

### Python Dictionaries

> Create a dictionary
```python
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict)

{'brand': 'Ford', 'model': 'Mustang', 'year': 1964}
```

> Access the items of a dictionary
```python 
eg1:thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
x = thisdict["model"]
print(x)

rs1:Mustang

eg2:
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
for k,v in thisdict:
	print(k, v)

rs2:
brand Ford
model Mustang
year 1964
```

> Change the value of specific item in a dictionary
```python
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}

thisdict["year"] = 2018
print(thisdict)

{'brand': 'Ford', 'model': 'Mustang', 'year': 2018}
```

> Print all key names in a dictionary,one by one
```python
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
for x in thisdict:
	print(x)

brand
model
year
```

> Print all values in a dictionary,one by one
```python
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
for x in thisdict:
	print(thisdict[x])

Ford
Mustang
1964
```

> Using the values() function to return values of dictionary
```python
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
for x in thisdict.values():
	print(x)

Ford
Mustang
1964
```

> Loop through both keys an values,by using the items() function
```python
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
for x, y in thisdict.items():
	print(x, y)

brand Ford
model Mustang
year 1964
```

> Check if a key exists
```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
if "model" in thisdict:
	print("Yes, 'model' is one of the keys in the thisdict dictionary")

Yes, 'model' is one of the keys in the thisdict dictionary
```

> Get the length of a dictionary
```python
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(len(thisdict))

3
```

> Add an item to a dictionary
```python
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict["color"] = "red"
print(thisdict)

{'brand': 'Ford', 'model': 'Mustang', 'year': 1964, 'color': 'red'}
```

> Remove an item from a dictionary
```python
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.pop("model")
print(thisdict)

{'brand': 'Ford', 'year': 1964}
```

> Empty a dictionary
```python
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.clear()
print(thisdict)

{}
```

> Using the dict() constructor to create a dictionary
```python
thisdict = dict(brand="Ford", model="Mustang", year=1964)
# note that keywords are not string literals
# note the use of equals rather than colon for the assignment
print(thisdict)

{'brand': 'Ford', 'model': 'Mustang', 'year': 1964}
```




### Python If ... Else

> The if statement
```python
a = 33
b = 200

if b > a:
	print("b is greater than a")

b is greater than a
```

> The elif statement
```python
a = 33
b = 33
if b > a:
	print("b is greater than a")
elif a == b:
	print("a and b are equal")

a and b are equal
```

> The else statement
```python
a = 200
b = 33
if b > a:
	print("b is greater than a")
elif a == b:
	print("a and b are equal")
else:
	print("a is greater than b")

a is greater than b
```

> Short hand if 
```python
a = 200
b = 33
if a > b: print("a is greater than b")

"a is greater than b"
```

> Short hand if ... else
```python
a = 2
b = 330
print("A") if a > b else print("B")

B
```

> The and keyword
```python
a = 200
b = 33
c = 500
if a > b and c > a:
	print("Both conditions are True")

Both conditions are True
```

> The or keyworda = 33
b = 200

if b > a:
	print("b is greater than a")

b is greater than a
```python
a = 200
b = 33
c = 500
if a > b or a > c:
	print("At least one of the conditions is True")

At least one of the conditions is True
```



### Python While Loop

> The while loop
```python
i = 1
while i < 6:
	print(i)
	i += 1

1
2
3
4
5
```

> Using the break statement in a while loop
```python
i = 1
while i < 6:
	print(i)
	if (i == 3):
		break
	i += 1

1
2
3
```

> Using the continue statement in a while loop
```python
i = 0
while i < 6:
	i += 1
	if i == 3:
		continue
	print(i)
# Note that number 3 is missing in the result

1
2
4
5
6
```



### Python For Loop

> The for loop
```python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
	print(x)

apple
banana
cherry
```

> Loop through a string
```python
for x in "banana":
	print(x)

b
a
n
a
n
a
```

> Using the break statement in a for loop
```python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
	print(x) 
	if x == "banana":
		break

apple
banana
```

> Using the continue statement in a for loop
```python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
	if x == "banana":
		continue
	print(x) 

apple
cherry
```

> Using the range() function in a for loop
```python
for x in range(6):
	print(x)

0
1
2
3
4
5
```

> Else in for loop
```python
for x in range(6):
	print(x)
else:
	print("Finally finished!")

0
1
2
3
4
5
Finally finished!
```

> Nested for loop
```python
adj = ["red", "big", "tasty"]
fruits = ["apple", "banana", "cherry"]

for x in adj:
	for y in fruits:
		print(x, y)


​
​
red apple
red banana
red cherry
big apple
big banana
big cherry
tasty apple
tasty banana
tasty cherry
```



### Python Functions

> Create and call a function
```python
def my_function():
	print("Hello from a function")
my_function()

Hello from a function
```

> Function parameters
```python
def my_function(fname):
	print(fname + " Refsnes")

my_function("Emil")
my_function("Tobias")
my_function("Linus")

Emil Refsnes
Tobias Refsnes
Linus Refsnes
```

> Default parameter value
```python
def my_function(country = "Norway"):
	print("I am from " + country)

my_function("Sweden")
my_function("India")
my_function()
my_function("Brazil")

I am from Sweden
I am from India
I am from Norway
I am from Brazil
```

> Let a function return a value
```python
def my_function(x):
	return 5 * x

print(my_function(3))
print(my_function(5))
print(my_function(9))

15
25
45
```

> Recursion
```python
def tri_recursion(k):
	if(k > 0):
		result = k + tri_recursion(k - 1)
		print(result)
	else:
		result = 0
	return result

print("\n\nRecursion Example Results")
tri_recursion(6)

Recursion Example Results
1
3
6
10
15
21
```



### Python Lambda

> A lambda function that adds 10 to the number passed in as an argument
```python
x = lambda a: a + 10
print(x(5))

15
```

> A lambda function that multiplies argument a with argument b
```python
x = lambda a, b: a * b
print(x(5, 6))

30
```

> A lambda function that sums argument a,b and c
```python
x = lambda a, b, c: a + b + c
print(x(5, 6, 2))

13
```



### Python Arrays

> Create an array
```python
cars = ["Ford", "Volvo", "BMW"]
print(cars)

['Ford', 'Volvo', 'BMW']
```

> Access the elements of an array
```python
cars = ["Ford", "Volvo", "BMW"]
x = cars[0]
print(x)

Ford
```

> Change the value of an array element
```python
cars = ["Ford", "Volvo", "BMW"]
cars[0] = "Toyota"
print(cars)

['Toyota', 'Volvo', 'BMW']
```

> Get the length of an array
```python
cars = ["Ford", "Volvo", "BMW"]
x = len(cars)
print(x)

3
```

> Loop through all elements os an array
```python
cars = ["Ford", "Volvo", "BMW"]
for x in cars:
	print(x)

Ford
Volvo
BMW
```

> Add an element to an array
```python
cars = ["Ford", "Volvo", "BMW"]
cars.append("Honda")
print(cars)

['Ford', 'Volvo', 'BMW', 'Honda']
```

> Remove an element from an array
```python
cars = ["Ford", "Volvo", "BMW"]
cars.pop(1)
print(cars)

['Ford', 'BMW']
```



### Python Classes and Objects

> Create a class
```python
class MyClass:
	x = 5
print(MyClass)

<class '__main__.MyClass'>
```

> Create an object
```python
Class MyClass:
	x = 5
p1 = MyClass()
print(p1.x)

5
```

> The __init__() Function
```python
class Person:
	def __init__(self, name, age):
		self.name = name
		self.age = age

p1 = Person('John', 35)
print(p1.name)
print(p2.age)

John
35
```

> Create Object methods
```python
class Person:
	def __init__(self, name, age):
		self.name = name
		self.age = age

	def myfunc(self):
		print("Hello my name is " + self.name)

p1 = Person("John", 36)
p1.myfunc()

Hello my name is John
```

> The self parameter
```python
class Person:
	def __init__(mysillyobject, name, age):
		mysillyobject.name = name
		mysillyobject.age = age

	def myfunc(abc):
		print("Hello my name is " + abc.name)

p1 = Person("John", 36)
p1.myfunc()

Hello my name is John
```

> Modify object properties
```python
class Person:
	def __init__(self, name, age):
		self.name = name
		self.age = age

	def myfunc(self):
		print("Hello my name is " + self.name)

p1 = Person("John", 36)
p1.age = 40
print(p1.age)

40
```

> Delete object Properties
```python
class Person:
	def __init__(self, name, age):
		self.name = name
		self.age = age

	def myfunc(self):
		print("Hello my name is " + self.name)

p1 = Person("John", 36)
# 删除对象p1的属性age
del p1.age
# 打印p1.age属性
print(p1.age)

Traceback (most recent call last):
  File "demo_class7.py", line 13, in <module>
    print(p1.age)
AttributeError: 'Person' object has no attribute 'age'
```

> Delete an object
```python
class Person:
	def __init__(self, name, age):
		self.name = name
		self.age = age

	def myfunc(self):
		print("Hello my name is " + self.name)

p1 = Person("John", 36)
# 删除p1对象
del p1
# 打印p1对象
print(p1)

Traceback (most recent call last):
	File "demo_class8.py", line 13, in <module>
		print(p1)
NameError: 'p1' is not defined
```



### Python Iterators

> Return an iterator from a tuple
```python
mytuple = ("apple", "banana", "cherry")
myit = iter(mytuple)

print(next(myit))
print(next(myit))
print(next(myit))

apple
banana
cherry
```

> Return an iterator from a string
```python
mystr = "banana"
myit = iter(mystr)

print(next(myit))
print(next(myit))
print(next(myit))
print(next(myit))
print(next(myit))
print(next(myit))


b
a
n
a
n
a
```

> Loop through an iterator
```python
mytuple = ("apple", "banana", "cherry")

for x in mytuple:
	print(x)

apple
banana
cherry
```

> Create an iterator
```python
class MyNumbers:
	def __iter__(self):
		self.a = 1
		return self

	def __next__(self):
		x = self.a
		self.a += 1
		return x

myclass = MyNumbers()
myiter = iter(myclass)

print(next(myiter))
print(next(myiter))
print(next(myiter))
print(next(myiter))
print(next(myiter))


1
2
3
4
5
```

> Stop iteration
```python
class MyNumbers:
	def __iter__(self):
		self.a = 1
		return self

	def __next__(self):
		if self.a <= 20:
			x = self.a
			self.a += 1
			return x
		else:
			raise StopIteration

myclass = MyNumbers()
myiter = iter(myclass)

for x in myiter:
	print(x)

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
```



### Python Modules

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```



### Python Dates


> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```



### Python Math


> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```



### Python JSON


> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```



### Python RegEx


> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```



### Python PIP


> 
```python

```



### Python Try Except


> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```



### Python Files


> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```



### Python MySQL

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```



### Python MongoDB

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```

> 
```python

```
