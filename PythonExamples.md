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

> Use a module
```python
import mymodule
mymodule.greeting('Jonathan')

Hello, Jonathan
```

> Variables in module
```python
import mymodule

a = mymodule.person1["age"]
print(a)

36
```

> Re-naming a module
```python
import mymodule as mx

a = mx.person1["age"]
print(a)

36
```

> Built-in modules
```python
import platform

x = platform.system()
print(x)

Windows
```

> Using the dir() function
```python
import platform

x = dir(platform)
print(x)

['DEV_NULL', '_UNIXCONFDIR', 'WIN32_CLIENT_RELEASES', 'WIN32_SERVER_RELEASES', '__builtins__', '__cached__', '__copyright__', '__doc__', '__file__', '__loader__', '__name__', '__package __', '__spec__', '__version__', '_default_architecture', '_dist_try_harder', '_follow_symlinks', '_ironpython26_sys_version_parser', '_ironpython_sys_version_parser', '_java_getprop', '_libc_search', '_linux_distribution', '_lsb_release_version', '_mac_ver_xml', '_node', '_norm_version', '_perse_release_file', '_platform', '_platform_cache', '_pypy_sys_version_parser', '_release_filename', '_release_version', '_supported_dists', '_sys_version', '_sys_version_cache', '_sys_version_parser', '_syscmd_file', '_syscmd_uname', '_syscmd_ver', '_uname_cache', '_ver_output', 'architecture', 'collections', 'dist', 'java_ver', 'libc_ver', 'linux_distribution', 'mac_ver', 'machine', 'node', 'os', 'platform', 'popen', 'processor', 'python_branch', 'python_build', 'python_compiler', 'python_implementation', 'python_revision', 'python_version', 'python_version_tuple', 're', 'release', 'subprocess', 'sys', 'system', 'system_aliases', 'uname', 'uname_result', 'version', 'warnings', 'win32_ver']
```

> Import from module
```python
from mymodule import person1
print(person1["age"])

36
```



### Python Dates


> Import the datetime module and display the current date
```python
import datetime
x = datetime.datetime.now()
print(x)

2020-07-09 10:49:32.116713
```

> Return the year and name of weekday
```python
import datetime

x = datetime.datetime.now()

print(x.year)
print(x.strftime("%A"))

2020
Thursday
```

> Create a date object
```python
import datetime
x = datetime.datetime(2020, 5, 17)
print(x)

2020-05-17 00:00:00
```

> The strftime() Method
```python
import datetime
x = datetime.datetime(2018, 6, 1)
print(x.strftime("%B"))

June
```



### Python Math


> Find the lowest and highest value in an iterable
```python
x = min(5, 10, 25)
y = max(5, 10, 25)

print(x)
print(y)

50
25
```

> Return the absolute value of a number
```python
x = abs(-7.25)
print(x)

7.25
```

> Return the value of x to the power of y (x^y)
```python
x = pow(4, 3)
print(x)

64
```

> Return the square root of a number
```python
import math
x = math.sqrt(64)
print(x)

8.0
```

> Round a number upwards and downwards to its nearest integer
```python
#Import math library
import math

#Round a number upward to its nearest integer
x = math.ceil(1.4)

#Round a number downward to its nearest integer
y = math.floor(1.4)

print(x)
print(y)


2
1
```

> Return the value of PI
```python
import math
x = math.pi
print(x)

3.141592653589793
```



### Python JSON

> Convert from Json to Python
```python loads
import json

# some JSON:
x = '{ "name":"John", "age":30, "city":"New York"}'

# parse x:
y = json.loads(x)

# the result is a Python dictionary:
print(y["age"])


30
```

> Convert from Python to Json
```python
import json

# a Python object (dict):
x = {
  "name": "John",
  "age": 30,
  "city": "New York"
}

# convert into JSON:
y = json.dumps(x)

# the result is a JSON string:
print(y)

{"name": "John", "age": 30, "city": "New York"}
```

> Convert Python objects into Json strings
```python
import json

print(json.dumps({"name": "John", "age": 30}))
print(json.dumps(["apple", "bananas"]))
print(json.dumps(("apple", "bananas")))
print(json.dumps("hello"))
print(json.dumps(42))
print(json.dumps(31.76))
print(json.dumps(True))
print(json.dumps(False))
print(json.dumps(None))


{"name": "John", "age": 30}
["apple", "bananas"]
["apple", "bananas"]
"hello"
42
31.76
true
false
null
```

> Convert a Python object containing all the legal data types
```python
import json

x = {
  "name": "John",
  "age": 30,
  "married": True,
  "divorced": False,
  "children": ("Ann","Billy"),
  "pets": None,
  "cars": [
    {"model": "BMW 230", "mpg": 27.5},
    {"model": "Ford Edge", "mpg": 24.1}
  ]
}

# convert into JSON:
y = json.dumps(x)

# the result is a JSON string:
print(y)

{"name": "John", "age": 30, "married": true, "divorced": false, "children": ["Ann","Billy"], "pets": null, "cars": [{"model": "BMW 230", "mpg": 27.5}, {"model": "Ford Edge", "mpg": 24.1}]}
```

> Use the indent parameter to define the numbers of indents
```python
import json

x = {
  "name": "John",
  "age": 30,
  "married": True,
  "divorced": False,
  "children": ("Ann","Billy"),
  "pets": None,
  "cars": [
    {"model": "BMW 230", "mpg": 27.5},
    {"model": "Ford Edge", "mpg": 24.1}
  ]
}

# use four indents to make it easier to read the result:
print(json.dumps(x, indent=4))


{
    "name": "John",
    "age": 30,
    "married": true,
    "divorced": false,
    "children": [
        "Ann",
        "Billy"
    ],
    "pets": null,
    "cars": [
        {
            "model": "BMW 230",
            "mpg": 27.5
        },
        {
            "model": "Ford Edge",
            "mpg": 24.1
        }
    ]
}
```

> Use the separators parameter to change the default separator
```python
import json

x = {
  "name": "John",
  "age": 30,
  "married": True,
  "divorced": False,
  "children": ("Ann","Billy"),
  "pets": None,
  "cars": [
    {"model": "BMW 230", "mpg": 27.5},
    {"model": "Ford Edge", "mpg": 24.1}
  ]
}

# use . and a space to separate objects, and a space, a = and a space to separate keys from their values:
print(json.dumps(x, indent=4, separators=(". ", " = ")))

{
    "name" = "John".
    "age" = 30.
    "married" = true.
    "divorced" = false.
    "children" = [
        "Ann".
        "Billy"
    ],
    "pets" = null.
    "cars" = [
        {
            "model" = "BMW 230".
            "mpg" = 27.5
        }.
        {
            "model" = "Ford Edge".
            "mpg" = 24.1
        }
    ]
}
```

> Use the sort_keys parameter to specify if the result should be sorted or not
```python
import json

x = {
  "name": "John",
  "age": 30,
  "married": True,
  "divorced": False,
  "children": ("Ann","Billy"),
  "pets": None,
  "cars": [
    {"model": "BMW 230", "mpg": 27.5},
    {"model": "Ford Edge", "mpg": 24.1}
  ]
}

# sort the result alphabetically by keys:
print(json.dumps(x, indent=4, sort_keys=True))

{
    "age": 30,
    "cars": [
        {
            "model": "BMW 230",
            "mpg": 27.5
        },
        {
            "model": "Ford Edge",
            "mpg": 24.1
        }
    ],
    "children": [
        "Ann",
        "Billy"
    ],
    "divorced": false,
    "married": true,
    "name": "John",
    "pets": null
}
```



### Python RegEx

> Search a string to see if it starts with "The" and ends with "Spain"
```python
import re

#Check if the string starts with "The" and ends with "Spain":

txt = "The rain in Spain"
x = re.search("^The.*Spain$", txt)

if x:
  print("YES! We have a match!")
else:
  print("No match")

YES! We have a match!
```

> Using the findall() function
```python
import re

#Return a list containing every occurrence of "ai":

txt = "The rain in Spain"
x = re.findall("ai", txt)
print(x)

['ai', 'ai']
```

> Using the search() function
```python
import re
txt = "The rain in Spain"
x = re.search("\s", txt)
print("The first white-space character is located in position:", x.start()) 

The first white-space character is located in position: 3
```

> Using the split() function
```python
import re

#Split the string at every white-space character:

txt = "The rain in Spain"
x = re.split("\s", txt)
print(x)

['The', 'rain', 'in', 'Spain']
```

> Using the sub() function
```python
import re

#Replace all white-space characters with the digit "9":

txt = "The rain in Spain"
x = re.sub("\s", "9", txt)
print(x)

The9rain9in9Spain
```



### Python PIP

> Using a package
```python
import camelcase

c = camelcase.CamelCase()

txt = "lorem ipsum dolor sit amet"

print(c.hump(txt))

#This method capitalizes the first letter of each word.


Lorem Ipsum Dolor Sit Amet
```



### Python Try Except

> When an error occurs,print a message
```python
#The try block will generate an error, because x is not defined:

try:
  print(x)
except:
  print("An exception occurred")

An exception occurred
```

> Many exceptions
```python
#The try block will generate a NameError, because x is not defined:

try:
  print(x)
except NameError:
  print("Variable x is not defined")
except:
  print("Something else went wrong")

Variable x is not defined
```

> Use the else keyword to define a block of code to be executed if no errors were raised
```python
#The try block does not raise any errors, so the else block is executed:

try:
  print("Hello")
except:
  print("Something went wrong")
else:
  print("Nothing went wrong")

Hello
Nothing went wrong
```

> Use the finally block to execute code regardless if the try block raises an error or not
```python
#The finally block gets executed no matter if the try block raises any errors or not:

try:
  print(x)
except:
  print("Something went wrong")
finally:
  print("The 'try except' is finished")

Something went wrong
The 'try except' is finished
```



### Python Files


> Read a file
```python
f = open("demofile.txt", "r")
print(f.read())

Hello! Welcome to demofile.txt
This file is for testing purposes.
Good Luck!
```

> Read only parts of file
```python
f = open("demofile.txt", "r")
print(f.read(5))

Hello
```

> Read one line of file
```python
f = open("demofile.txt", "r")
print(f.readline())

Hello! Welcome to demofile.txt
```

> Loop through the lines of a file to read the whole file,line by line
```python
f = open("demofile.txt", "r")
for x in f:
  print(x)


Hello! Welcome to demofile.txt
This file is for testing purposes.
Good Luck!
```



### Python MySQL

> Create a connection to a database
```python
import mysql.connector
mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword"
)
print(mydb)

<mysql.connector.connection.MySQLConnection object ar 0x016645F0>
```

> Create a database in MySQL
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword"
)

mycursor = mydb.cursor()

mycursor.execute("CREATE DATABASE mydatabase")

#If this page is executed with no error, you have successfully created a database.
```

> Check if a database exist
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword"
)

mycursor = mydb.cursor()

mycursor.execute("SHOW DATABASES")

for x in mycursor:
  print(x)


('information_scheme',)
('mydatabase',)
('performance_schema',)
('sys',)
```

> Create a table 
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

mycursor.execute("CREATE TABLE customers (name VARCHAR(255), address VARCHAR(255))")

#If this page is executed with no error, you have successfully created a table named "customers".
```

> Check if a table exist
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

mycursor.execute("SHOW TABLES")

for x in mycursor:
     print(x)


('customers',)
```

> Create primary key when creating a table
```python # 在创建表的时候，某一个字段后添加属性 Primary key
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  password="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

mycursor.execute("CREATE TABLE customers (id INT AUTO_INCREMENT PRIMARY KEY, name VARCHAR(255), address VARCHAR(255))")

#If this page is executed with no error, the table "customers" now has a primary key
```

> Insert a record in a table 
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "INSERT INTO customers (name, address) VALUES (%s, %s)"
val = ("John", "Highway 21")

mycursor.execute(sql, val)

mydb.commit()

print(mycursor.rowcount, "record inserted.")


1 record inserted.
```

> Insert multiple rows
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "INSERT INTO customers (name, address) VALUES (%s, %s)"
val = [
 ('Peter', 'Lowstreet 4'),
 ('Amy', 'Apple st 652'),
 ('Hannah', 'Mountain 21'),
 ('Michael', 'Valley 345'),
 ('Sandy', 'Ocean blvd 2'),
 ('Betty', 'Green Grass 1'),
 ('Richard', 'Sky st 331'),
 ('Susan', 'One way 98'),
 ('Vicky', 'Yellow Garden 2'),
 ('Ben', 'Park Lane 38'),
 ('William', 'Central st 954'),
 ('Chuck', 'Main Road 989'),
 ('Viola', 'Sideway 1633')
]

mycursor.executemany(sql, val)

mydb.commit()

print(mycursor.rowcount, "record was inserted.")


13 record was inserted.
```

> Get inserted ID
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "INSERT INTO customers (name, address) VALUES (%s, %s)"
val = ("Michelle", "Blue Village")
mycursor.execute(sql, val)

mydb.commit()

print("1 record inserted, ID:", mycursor.lastrowid)


1 record inserted, ID: 15
```

> Select all records from a table
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

mycursor.execute("SELECT * FROM customers")

myresult = mycursor.fetchall()

for x in myresult:
  print(x)


(1, 'John', 'Highway 21')
(2, 'Peter', 'Lowstreet 27')
(3, 'Amy', 'Apple st 652')
(4, 'Hannah', 'Mountain 21')
(5, 'Michael', 'Valley 345')
(6, 'Sandy', 'Ocean blvd 2')
(7, 'Betty', 'Green Grass 1')
(8, 'Richard', 'Sky st 331')
(9, 'Susan', 'One way 98')
(10, 'Vicky', 'Yellow Garden 2')
(11, 'Ben', 'Park Lane 38')
(12, 'William', 'Central st 954')
(13, 'Chuck', 'Main Road 989')
(14, 'Viola', 'Sideway 1633')
(15, 'Michelle', 'Blue Village')
```

> Select only some of the columns in a table
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

mycursor.execute("SELECT name, address FROM customers")

myresult = mycursor.fetchall()

for x in myresult:
  print(x)


('John', 'Highway 21')
('Peter', 'Lowstreet 27')
('Amy', 'Apple st 652')
('Hannah', 'Mountain 21')
('Michael', 'Valley 345')
('Sandy', 'Ocean blvd 2')
('Betty', 'Green Grass 1')
('Richard', 'Sky st 331')
('Susan', 'One way 98')
('Vicky', 'Yellow Garden 2')
('Ben', 'Park Lane 38')
('William', 'Central st 954')
('Chuck', 'Main Road 989')
('Viola', 'Sideway 1633')
('Michelle', 'Blue Village')
```

> Use the fetchone() method to fetch only one row in a table
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

mycursor.execute("SELECT * FROM customers")

myresult = mycursor.fetchone()

print(myresult)


(1, 'John', 'Highway 21')
```

> Select with a filter
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "SELECT * FROM customers WHERE address = 'Park Lane 38'"

mycursor.execute(sql)

myresult = mycursor.fetchall()

for x in myresult:
  print(x)


(11, 'Ben', 'Park Lane 38')
```

> Wildcards characters (通配符)
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "SELECT * FROM customers WHERE address Like '%way%'"

mycursor.execute(sql)

myresult = mycursor.fetchall()

for x in myresult:
  print(x)


(1, 'John', 'Highway 21')
(9, 'Susan', 'One way 98')
(14, 'Viola', 'Sideway 1633')
```

> Prevent SQL injection  (防止SQL注入攻击)
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "SELECT * FROM customers WHERE address = %s"
adr = ("Yellow Garden 2", )

mycursor.execute(sql, adr)

myresult = mycursor.fetchall()

for x in myresult:
  print(x)


(10, 'Vicky', 'Yellow Garden 2')
```

> Sort the result of a table alphabetically
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "SELECT * FROM customers ORDER BY name"

mycursor.execute(sql)

myresult = mycursor.fetchall()

for x in myresult:
  print(x)


(3, 'Amy', 'Apple st 652')
(11, 'Ben', 'Park Lane 38')
(7, 'Betty', 'Green Grass 1')
(13, 'Chuck', 'Main Road 989')
(4, 'Hannah', 'Mountain 21')
(1, 'John', 'Highway 21')
(5, 'Michael', 'Valley 345')
(15, 'Michelle', 'Blue Village') (2, 'Peter', 'Lowstreet 27')
(8, 'Richard', 'Sky st 331')
(6, 'Sandy', 'Ocean blvd 2')
(9, 'Susan', 'One way 98')
(10, 'Vicky', 'Yellow Garden 2')
(14, 'Viola', 'Sideway 1633')
(12, 'William', 'Central st 954')
```

> Sort the result in a descending order (reverse alphabetically)
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "SELECT * FROM customers ORDER BY name DESC"

mycursor.execute(sql)

myresult = mycursor.fetchall()

for x in myresult:
  print(x)


(12, 'William', 'Central st 954') (14, 'Viola', 'Sideway 1633')
(10, 'Vicky', 'Yellow Garden 2')
(9, 'Susan', 'One way 98')
(6, 'Sandy', 'Ocean blvd 2')
(8, 'Richard', 'Sky st 331')
(2, 'Peter', 'Lowstreet 27')
(15, 'Michelle', 'Blue Village') (5, 'Michael', 'Valley 345')
(1, 'John', 'Highway 21')
(4, 'Hannah', 'Mountain 21')
(13, 'Chuck', 'Main Road 989')
(7, 'Betty', 'Green Grass 1')
(11, 'Ben', 'Park Lane 38')
(3, 'Amy', 'Apple st 652')
```

> Delete records from an existing table
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "DELETE FROM customers WHERE address = 'Mountain 21'"

mycursor.execute(sql)

mydb.commit()

print(mycursor.rowcount, "record(s) deleted")


1 record(s) deleted
```

> Prevent SQL injection
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "DELETE FROM customers WHERE address = %s"
adr = ("Yellow Garden 2", )

mycursor.execute(sql, adr)

mydb.commit()

print(mycursor.rowcount, "record(s) deleted")


1 record(s) deleted
```

> Delete an existing table
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "DROP TABLE customers"

mycursor.execute(sql)

#If this page was executed with no error(s), you have successfully deleted the "customers" table.

```

> Delete a table if it exist
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "DROP TABLE IF EXISTS customers"

mycursor.execute(sql)

#If this page was executed with no error(s), you have successfully deleted the "customers" table.

```

> Update existing records in a table 
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "UPDATE customers SET address = 'Canyon 123' WHERE address = 'Valley 345'"

mycursor.execute(sql)

mydb.commit()

print(mycursor.rowcount, "record(s) affected")

1 record(s) affected
```

> Prevent SQL injection
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "UPDATE customers SET address = %s WHERE address = %s"
val = ("Valley 345", "Canyon 123")

mycursor.execute(sql, val)

mydb.commit()

print(mycursor.rowcount, "record(s) affected")


1 record(s) affected
```

> Limit the number of recodes returned from a query
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

mycursor.execute("SELECT * FROM customers LIMIT 5")

myresult = mycursor.fetchall()

for x in myresult:
  print(x)


(1, 'John', 'Highway 21')
(2, 'Peter', 'Lowstreet 27')
(3, 'Amy', 'Apple st 652')
(4, 'Hannah', 'Mountain 21')
(5, 'Michael', 'Valley 345')
```

> Combine rows from two or more tables,based on a related column between them
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "SELECT \
  users.name AS user, \
  products.name AS favorite \
  FROM users \
  INNER JOIN products ON users.fav = products.id"

mycursor.execute(sql)

myresult = mycursor.fetchall()

for x in myresult:
  print(x)

('John', 'Chocolate Heaven')
('Peter', 'Chocolate Heaven')
('Amy', 'Tasty Lemon')
```

> LEFT JOIN
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "SELECT \
  users.name AS user, \
  products.name AS favorite \
  FROM users \
  LEFT JOIN products ON users.fav = products.id"

mycursor.execute(sql)

myresult = mycursor.fetchall()

for x in myresult:
  print(x)


('John', 'Chocolate Heaven')
('Peter', 'Chocolate Heaven')
('Amy', 'Tasty Lemon')
('Hannah', None)
('Michael', None)
```

> RIGHT JOIN
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "SELECT \
  users.name AS user, \
  products.name AS favorite \
  FROM users \
  RIGHT JOIN products ON users.fav = products.id"

mycursor.execute(sql)

myresult = mycursor.fetchall()

for x in myresult:
  print(x)


('John', 'Chocolate Heaven')
('Peter', 'Chocolate Heaven')
('Amy', 'Tasty Lemon')
(None, 'Vanilla Dreams')
```



### Python MongoDB

> Create database
```python
import pymongo

myclient = pymongo.MongoClient('mongodb://localhost:27017/')

mydb = myclient['mydatabase']

# database created!
```

> Check if a database exist
```python
import pymongo

myclient = pymongo.MongoClient('mongodb://localhost:27017/')

print(myclient.list_database_names())


['admin', 'local', 'mydatabase']
```

> Create a collection
```python
import pymongo

myclient = pymongo.MongoClient('mongodb://localhost:27017/')

mydb = myclient['mydatabase']

mycol = mydb["customers"]

# collection created!

```

> Check if a collection exist
```python
import pymongo

myclient = pymongo.MongoClient('mongodb://localhost:27017/')

mydb = myclient['mydatabase']

mycol = mydb["customers"]

print(mydb.list_collection_names())


['customers']
```

> Insert into collection
```python
import pymongo

myclient = pymongo.MongoClient('mongodb://localhost:27017/')
mydb = myclient['mydatabase']
mycol = mydb["customers"]

mydict = { "name": "John", "address": "Highway 37" }

x = mycol.insert_one(mydict)

print(x)


<pymongo.results.InsertOneResult object at 0x03D62918>
```

> Return the id filed
```python
import pymongo

myclient = pymongo.MongoClient('mongodb://localhost:27017/')
mydb = myclient['mydatabase']
mycol = mydb["customers"]

mydict = { "name": "Peter", "address": "Lowstreet 27" }

x = mycol.insert_one(mydict)

print(x.inserted_id)


5b1910482ddb101b7042fcd7
```

> Insert multiple documents
```python
import pymongo

myclient = pymongo.MongoClient("mongodb://localhost:27017/")
mydb = myclient["mydatabase"]
mycol = mydb["customers"]

mylist = [
  { "name": "Amy", "address": "Apple st 652"},
  { "name": "Hannah", "address": "Mountain 21"},
  { "name": "Michael", "address": "Valley 345"},
  { "name": "Sandy", "address": "Ocean blvd 2"},
  { "name": "Betty", "address": "Green Grass 1"},
  { "name": "Richard", "address": "Sky st 331"},
  { "name": "Susan", "address": "One way 98"},
  { "name": "Vicky", "address": "Yellow Garden 2"},
  { "name": "Ben", "address": "Park Lane 38"},
  { "name": "William", "address": "Central st 954"},
  { "name": "Chuck", "address": "Main Road 989"},
  { "name": "Viola", "address": "Sideway 1633"}
]

x = mycol.insert_many(mylist)

#print list of the _id values of the inserted documents:

print(x.inserted_ids)


[ObjectId('5b19112f2ddb101964065487'), ObjectId('5b19112f2ddb101964065488'), ObjectId('5b19112f2ddb101964065489'), ObjectId('5b19112f2ddb10196406548a'), ObjectId('5b19112f2ddb10196406548b'), ObjectId('5b19112f2ddb10196406548c'), ObjectId('5b19112f2ddb10196406548d'), ObjectId('5b19112f2ddb10196406548e'), ObjectId('5b19112f2ddb10196406548f'), ObjectId('5b19112f2ddb101964065490'), ObjectId('5b19112f2ddb101964065491'), 
ObjectId('5b19112f2ddb101964065492')]
```

> Insert multiple documents with specified IDs
```python
import pymongo

myclient = pymongo.MongoClient("mongodb://localhost:27017/")
mydb = myclient["mydatabase"]
mycol = mydb["customers"]

mylist = [
  { "_id": 1, "name": "John", "address": "Highway 37"},
  { "_id": 2, "name": "Peter", "address": "Lowstreet 27"},
  { "_id": 3, "name": "Amy", "address": "Apple st 652"},
  { "_id": 4, "name": "Hannah", "address": "Mountain 21"},
  { "_id": 5, "name": "Michael", "address": "Valley 345"},
  { "_id": 6, "name": "Sandy", "address": "Ocean blvd 2"},
  { "_id": 7, "name": "Betty", "address": "Green Grass 1"},
  { "_id": 8, "name": "Richard", "address": "Sky st 331"},
  { "_id": 9, "name": "Susan", "address": "One way 98"},
  { "_id": 10, "name": "Vicky", "address": "Yellow Garden 2"},
  { "_id": 11, "name": "Ben", "address": "Park Lane 38"},
  { "_id": 12, "name": "William", "address": "Central st 954"},
  { "_id": 13, "name": "Chuck", "address": "Main Road 989"},
  { "_id": 14, "name": "Viola", "address": "Sideway 1633"}
]

x = mycol.insert_many(mylist)

#print a list of the _id values of the inserted documents:
print(x.inserted_ids)


[1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14]
```

> Find the first document in the selection
```python
import pymongo

myclient = pymongo.MongoClient("mongodb://localhost:27017/")
mydb = myclient["mydatabase"]
mycol = mydb["customers"]

x mycol.find_one()

print(x)


{'_id': 1, 'name': 'John', 'address': 'Highway37'}
```

> Find all documents in the selection
```python
import pymongo

myclient = pymongo.MongoClient("mongodb://localhost:27017/")
mydb = myclient["mydatabase"]
mycol = mydb["customers"]

for x in mycol.find():
  print(x)


{'_id': 1, 'name': 'John', 'address': 'Highway37'}
{'_id': 2, 'name': 'Peter', 'address': 'Lowstreet 27'}
{'_id': 3, 'name': 'Amy', 'address': 'Apple st 652'}
{'_id': 4, 'name': 'Hannah', 'address': 'Mountain 21'}
{'_id': 5, 'name': 'Michael', 'address': 'Valley 345'}
{'_id': 6, 'name': 'Sandy', 'address': 'Ocean blvd 2'}
{'_id': 7, 'name': 'Betty', 'address': 'Green Grass 1'}
{'_id': 8, 'name': 'Richard', 'address': 'Sky st 331'}
{'_id': 9, 'name': 'Susan', 'address': 'One way 98'}
{'_id': 10, 'name': 'Vicky', 'address': 'Yellow Garden 2'}
{'_id': 11, 'name': 'Ben', 'address': 'Park Lane 38'}
{'_id': 12, 'name': 'William', 'address': 'Central st 954'}
{'_id': 13, 'name': 'Chuck', 'address': 'Main Road 989'}
{'_id': 14, 'name': 'Viola', 'address': 'Sideway 1633'}
```

> Find only some fields
```python
import pymongo

myclient = pymongo.MongoClient("mongodb://localhost:27017/")
mydb = myclient["mydatabase"]
mycol = mydb["customers"]

for x in mycol.find({},{ "_id": 0, "name": 1, "address": 1 }):
  print(x)


{'name': 'John', 'address': 'Highway37'}
{'name': 'Peter', 'address': 'Lowstreet 27'}
{'name': 'Amy', 'address': 'Apple st 652'}
{'name': 'Hannah', 'address': 'Mountain 21'}
{'name': 'Michael', 'address': 'Valley 345'}
{'name': 'Sandy', 'address': 'Ocean blvd 2'}
{'name': 'Betty', 'address': 'Green Grass 1'}
{'name': 'Richard', 'address': 'Sky st 331'}
{'name': 'Susan', 'address': 'One way 98'}
{'name': 'Vicky', 'address': 'Yellow Garden 2'}
{'name': 'Ben', 'address': 'Park Lane 38'}
{'name': 'William', 'address': 'Central st 954'}
{'name': 'Chuck', 'address': 'Main Road 989'}
{'name': 'Viola', 'address': 'Sideway 1633'}
```

> Filter the result
```python
import pymongo

myclient = pymongo.MongoClient("mongodb://localhost:27017/")
mydb = myclient["mydatabase"]
mycol = mydb["customers"]

myquery = { "address": "Park Lane 38" }

mydoc = mycol.find(myquery)

for x in mydoc:
  print(x)


{'_id': 11, 'name': 'Ben', 'address': 'Park Lane 38'}
```

> Advanced query
```python
import pymongo

myclient = pymongo.MongoClient("mongodb://localhost:27017/")
mydb = myclient["mydatabase"]
mycol = mydb["customers"]

#address greater than S:
myquery = { "address": {"$gt": "S"} }

mydoc = mycol.find(myquery)

for x in mydoc:
  print(x)


{'_id': 5, 'name': 'Michael', 'address': 'Valley 345'}
{'_id': 8, 'name': 'Richard', 'address': 'Sky st 331'}
{'_id': 10, 'name': 'Vicky', 'address': 'Yellow Garden 2'}
{'_id': 14, 'name': 'Viola', 'address': 'Sideway 1633'}
```

> Filter with regular expressions
```python
import pymongo

myclient = pymongo.MongoClient('mongodb://localhost:27017/')
mydb = myclient['mydatabase']
mycol = mydb['customers']

# address starts with S:
myquery = {'address': {'$regex': '^S'}}

mydoc = mycol.find(myquery)

for x in mydoc:
	print(x)

​
{'_id': 10, 'name': 'Richard', 'address': 'Sky st 331'}
{'_id': 14, 'name': 'Viola', 'address': 'Sideway 1633'}
```

> Sort the result alphabetically(字母顺序排序检索结果)
```python
import pymongo
myclient = pymongo.MongoClient('mongodb://localhost:27017')
mydb = myclient['mydatabase']
mycol = mydb['customers']

mydoc = mycol.find().sort('name')

for x in mydoc:
	print(x)


{'_id': 3, 'name': 'Amy', 'address': 'Apple st 652'}
{'_id': 11, 'name': 'Ben', 'address': 'Park Lane 38'}
{'_id': 7, 'name': 'Betty', 'address': 'Green Grass 1'}
{'_id': 13, 'name': 'Chuck', 'address': 'Main Road 989'}
{'_id': 4, 'name': 'Hannah', 'address': 'Mountain 21'}
{'_id': 1, 'name': 'John', 'address': 'Highway37'}
{'_id': 5, 'name': 'Michael', 'address': 'Valley 345'}
{'_id': 2, 'name': 'Peter', 'address': 'Lowstreet 27'}
{'_id': 8, 'name': 'Richard', 'address': 'Sky st 331'}
{'_id': 6, 'name': 'Sandy', 'address': 'Ocean blvd 2'}
{'_id': 9, 'name': 'Susan', 'address': 'One way 98'}
{'_id': 10, 'name': 'Vicky', 'address': 'Yellow Garden 2'}
{'_id': 14, 'name': 'Viola', 'address': 'Sideway 1633'}
{'_id': 12, 'name': 'William', 'address': 'Central st 954'}
```

> Sort the result descending(reverse alphabetically)
```python
import pymongo

myclient = pymongo.MongoClient('mongodb://localhost:27017')
mydb = myclient['mydatabase']
mycol = mydb['customers']

mydoc = mycol.find().sort('name', -1)

for x in mydoc:
	print(x)


{'_id': 12, 'name': 'William', 'address': 'Central st 954'}
{'_id': 14, 'name': 'Viola', 'address': 'Sideway 1633'}
{'_id': 10, 'name': 'Vicky', 'address': 'Yellow Garden 2'}
{'_id': 9, 'name': 'Susan', 'address': 'One way 98'}
{'_id': 6, 'name': 'Sandy', 'address': 'Ocean blvd 2'}
{'_id': 8, 'name': 'Richard', 'address': 'Sky st 331'}
{'_id': 2, 'name': 'Peter', 'address': 'Lowstreet 27'}
{'_id': 5, 'name': 'Michael', 'address': 'Valley 345'}
{'_id': 1, 'name': 'John', 'address': 'Highway37'}
{'_id': 4, 'name': 'Hannah', 'address': 'Mountain 21'}
{'_id': 13, 'name': 'Chuck', 'address': 'Main Road 989'}
{'_id': 7, 'name': 'Betty', 'address': 'Green Grass 1'}
{'_id': 11, 'name': 'Ben', 'address': 'Park Lane 38'}
{'_id': 3, 'name': 'Amy', 'address': 'Apple st 652'}
```

> Delete document
```python
import pymongo

myclient = pymongo.MongoClient('mongodb://localhost:27017')
mydb = myclient['mydatabase']
mycol = mydb['customers']

myquery = {'address': 'Mountain 21'}

mycol.delete_one(myquery)

# print the customers collection after the deletion:
for x in mycol.find():
	print(x)


{'_id': 1, 'name': 'John', 'address': 'Highway37'}
{'_id': 2, 'name': 'Peter', 'address': 'Lowstreet 27'}
{'_id': 3, 'name': 'Amy', 'address': 'Apple st 652'}
{'_id': 5, 'name': 'Michael', 'address': 'Valley 345'}
{'_id': 6, 'name': 'Sandy', 'address': 'Ocean blvd 2'}
{'_id': 7, 'name': 'Betty', 'address': 'Green Grass 1'}
{'_id': 8, 'name': 'Richard', 'address': 'Sky st 331'}
{'_id': 9, 'name': 'Susan', 'address': 'One way 98'}
{'_id': 10, 'name': 'Vicky', 'address': 'Yellow Garden 2'}
{'_id': 11, 'name': 'Ben', 'address': 'Park Lane 38'}
{'_id': 12, 'name': 'William', 'address': 'Central st 954'}
{'_id': 13, 'name': 'Chuck', 'address': 'Main Road 989'}
{'_id': 14, 'name': 'Viola', 'address': 'Sideway 1633'}
```

> Delete many documents
```python
import pymongo

myclient = pymongo.MongoClient('mongodb://localhost:27017')
mydb = myclient['mydatabase']
mycol = mydb['customers']

myquery = {'address': {'$regex': '^S'}}

x = mycol.delete_many(myquery)

print(x.deleted_count, 'documents deleted')


2 documents deleted.
```

> Delete all documents in a collection
```python
import pymongo

myclient = pymongo.MongoClient('mongodb://localhost:27017')
mydb = myclient['mydatabase']
mycol = mydb['customers']

x = mycol.delete({})

print(x.deleted_count, 'documents deleted')


11 documents deleted.
```

> Delete a collection
```python
import pymongo

myclient = pymongo.MongoClient('mongodb://localhost:27017')
mydb = myclient['mydatabase']
mycol = mydb['customers']

mycol.drop()
```

> Update a document
```python
import pymongo

myclient = pymongo.MongoClient('mongodb://localhost:27017')
mydb = myclient['mydatabase']
mycol = mydb['customers']

myquery = {'address': 'Valley 345'}
newValues = {'$set': {'address': 'Canyon 123'}}

mycol.update_one(myquery, newValues)

# print 'customers' after the update
for x in mycol.find():
	print(x)


{'_id': 1, 'name': 'John', 'address': 'Highway37'}
{'_id': 2, 'name': 'Peter', 'address': 'Lowstreet 27'}
{'_id': 3, 'name': 'Amy', 'address': 'Apple st 652'}
{'_id': 4, 'name': 'Hannah', 'address': 'Mountain 21'}
{'_id': 5, 'name': 'Michael', 'address': 'Canyon 123'}
{'_id': 6, 'name': 'Sandy', 'address': 'Ocean blvd 2'}
{'_id': 7, 'name': 'Betty', 'address': 'Green Grass 1'}
{'_id': 8, 'name': 'Richard', 'address': 'Sky st 331'}
{'_id': 9, 'name': 'Susan', 'address': 'One way 98'}
{'_id': 10, 'name': 'Vicky', 'address': 'Yellow Garden 2'}
{'_id': 11, 'name': 'Ben', 'address': 'Park Lane 38'}
{'_id': 12, 'name': 'William', 'address': 'Central st 954'}
{'_id': 13, 'name': 'Chuck', 'address': 'Main Road 989'}
{'_id': 14, 'name': 'Viola', 'address': 'Sideway 1633'}
```

> Update many/all document
```python
import pymongo

myclient = pymongo.MongoClient("mongodb://localhost:27017/")
mydb = myclient["mydatabase"]
mycol = mydb["customers"]

myquery = {'address': {'$regex': '^S'}}

newValues = {'$set': {'name': 'Minnie'}}

x = mycol.update_many(myquery, newValues)

print(x.modified_count, 'documents updated.')


2 documents updated.
```

> Limit the result
```python
import pymongo

myclient = pymongo.MongoClient("mongodb://localhost:27017/")
mydb = myclient["mydatabase"]
mycol = mydb["customers"]

myresult = mycol.find().find().limit(5)

# print the result
for x in myresult:
	print(x)


{'_id': 1, 'name': 'John', 'address': 'Highway37'}
{'_id': 2, 'name': 'Peter', 'address': 'Lowstreet 27'}
{'_id': 3, 'name': 'Amy', 'address': 'Apple st 652'}
{'_id': 4, 'name': 'Hannah', 'address': 'Mountain 21'}
{'_id': 5, 'name': 'Michael', 'address': 'Valley 345'}
```
