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

```
