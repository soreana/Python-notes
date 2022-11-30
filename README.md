# Python-notes


In python result of the `/` is float !!!!!!!!!!!!!!

The truncated division operator, //, also works on floating point numbers. It truncates to the nearest integer, but still produces a floating point result. Thus 7.0 // 3.0 is 2.0.

for example:

```python

print( 10 / 3 ) # prints 3.333333333
print( 10 // 3) # prints 3

```

** is the power sign.

```python

print( 4**2 ) # prints 16
```


Functions are objects in Python. So if I print out what's the value of square, then Python is going to tell me that square is a function. So if I run my code, you can see that line 1 prints out function square.

```python

def square():
    return none
    
print(square) # outputs <function square>
```


type function shows the type of the variable.

```python
print(type("Hello, World!")) # prints <class 'str'>
print(type(20)) # prints <class 'int'>
print(type(3.2)) # prints <class 'float'>
print(type(True)) # prints <class 'bool'>
```

Use """ to split string in multiple lines.

```python
print("""This message will span
several lines
of the text.""")
```

When python casts float to int, it drops numbers after the dot. For example:

```python
int(3.999) # is 3
int(3.0) # is 3
int(-3.9999) # is -3
```


Get input:
```python
n = input("Please enter your name: ") # It always reads string. you should cast it if you want to convert it to another type.
print("Hello", n)
```

For loop examples:
```python
for _ in range(3): # runs three time
    ...
    
for i in range(5): # range returnes a sequence of [0, 1, 2, 3, 4] (last item is exclusive)
    ...

for i in range(1, 5): # now it returnes a sequence of [1, 2, 3, 4]
    ...
```

How import works

```python
import random

prob = random.random()
print(prob)

diceThrow = random.randrange(1,7)       # return an int, one of 1,2,3,4,5,6
print(diceThrow)
```

```python
from random import random, randrange

prob = random()
print(prob)

diceThrow = randrange(1,7)       # return an int, one of 1,2,3,4,5,6
print(diceThrow)

```


Tuple vs List: 
Tuple is immutable, but the list is not.

```python
t = (5,)
print(type(t)) # prints <class 'tuple'>

l = ["hello", 2.0, 5, [10, 20]]
print(type(l)) # prints <class 'list'>
```

```python
t = (5,) # this is a tuple.
t = (5)  # this is an integer. Python can't understand if if was the (2+3) or it is a tuple.
t = ()   # this is an empty tuple.
```

Slice operator: syntax [from`(inclusive)`:to`(exclusive)`]

```python
singers = "Peter, Paul, and Mary"
print(singers[7:11]) # It prints Paul, index five is not included!

fruit = "banana"
print(fruit[:3]) # ban, again index 3 is not included
print(fruit[3:]) # ana

L = [0.34, '6', 'SI106', 'Python', -2]
print(L[1:-1]) # prints [ '6', 'SI106', 'Python']
```

Concatenation:

```python
print([1,2] + [3,4]) # prints [1,2, 3,4]

print([0, 1] * 4) # prints [0, 1, 0, 1, 0, 1, 0, 1]

```

Count:
It is the same in String and Lists

```python
a = "I have had an apple on my desk before!"
z = ['atoms', 4, 'neutron', 6, 'proton', 4, 'electron', 4, 'electron', 'atoms']

print(a.count("e")) # prints 5
print(a.count("ha")) # prints 2
print(z.count(4)) # prints 3

```

Index:
It throws an error if it couldn't find the key

```python
music = "Pull out your music and dancing can begin"
bio = ["Metatarsal", "Metatarsal", "Fibula", [], "Tibia", "Tibia", 43, "Femur", "Occipital", "Metatarsal"]

print(music.index("m"))
print(music.index("your"))

print(bio.index("Metatarsal"))
print(bio.index([]))
print(bio.index(43))

seasons = ["winter", "spring", "summer", "fall"]

print(seasons.index("autumn"))  #Error!
```

Splitting:

```python
song = "The rain in Spain..."
wds = song.split() # it uses space as splitter by default.

song = "The rain in Spain..."
wds = song.split('ai') # it uses ai as splitter.
```

Joining:

```python
wds = ["red", "blue", "green"]
glue = ';'
s = glue.join(wds) 
print(s) # prints red;blue;green
print(wds) # join doesn't have any effect one the wds

print("".join(wds)) # prints redbluegreen

```

In operator:

```python
print('p' in 'apple') # returns True
print('' in 'a') # returns True
print('' in 'apple') # returns True
print('x' not in 'apple') # returns True
print("a" in ["a", "b", "c", "d"]) # returns True
print(9 in [3, 2, 9, 10, 9.0]) # returns True
print('wow' not in ['gee wiz', 'gosh golly', 'wow', 'amazing']) # returns Tru
```

Mutablity:

```python
alist = ['a', 'b', 'c', 'd', 'e', 'f']
alist[1:3] = ['x', 'y']
print(alist) # prints ['a', 'x', 'y', 'd', 'e', 'f']

alist[1:3] = [] # This assignment deletes elements 1 and 2 but it is better to use the del statement *1
print(alist) # prints ['a', 'd', 'e', 'f']

alist = ['a', 'd', 'f']
alist[1:1] = ['b', 'c']
print(alist) # prints ['a', 'b', 'c', 'd', 'f']

alist[4:4] = ['e']
print(alist) # prints ['a', 'b', 'c', 'd', 'e', 'f']

*1
a = ['one', 'two', 'three']
del a[1]
print(a) # prints ['one', 'three']

alist = ['a', 'b', 'c', 'd', 'e', 'f']
del alist[1:5]
print(alist) # prints ['a', 'f']
```

But Strings are immutable:

```python
greeting = "Hello, world!"
greeting[0] = 'J' # Results TypeError: 'str' does not support item assignment on line 2
```

Tuples are also immutable:
```python
julia = ("X", "Y")
julia[0] = 'X'  # TypeError: 'tuple' object does not support item assignment
```

Refrences

```python
a = "banana"
b = "banana"

print(a is b) # prints true

print(id(a)) # prints 2
print(id(b)) # prints 2

a = [81,82,83]
b = [81,82,83]

print(a is b) # prints False

print(a == b) # prints True

print(id(a)) # prints 3
print(id(b)) # prints 4

```

Cloning a List:
The slice operator, always grabs some part of a list, and **makes a new list** using those items that have been grabbed. So, if we execute the following code, then we have a clone of a.

```python
a = [1, 2, 3, 4, 5]
b = a[:] # Now, b is the clone of the a
```

Mutating methods:

```python
mylist = []
mylist.append(5)
mylist.append(27)
mylist.append(3)
mylist.append(12)
print(mylist) # prints [5, 27, 3, 12]

mylist.insert(1, 12)
print(mylist) # prints [5, 12, 27, 3, 12]
print(mylist.count(12)) # prints 2

print(mylist.index(3)) # prints 3
print(mylist.count(5)) # prints 1

mylist.reverse() # it is in-place
print(mylist) # prints [12, 3, 27, 12, 5]

mylist.sort() # it is in-place
print(mylist) # prints [3, 5, 12, 12, 27]

mylist.remove(5) # removes 5 not an object at index 5
print(mylist) # prints [3, 12, 12, 27]

lastitem = mylist.pop() 
print(lastitem) # prints 27
print(mylist) # prints [3, 12, 12]
```

**Important:** Concatenation with + operator creates a new list, but the append function add the element to the end of the array. It doesn't create a new list.

The fucking Python language doesn't do the same with (arr) + (arr) and (arr) += (arr). In case of (arr) + (arr) it concatenate the arrays and creates new object. But in (arr) += (arr) it append the second array to the first one. There isn't any new object.

String mutation:

It doesn't have any effect on the String, it always generates new string.

```python
ss = "Hello, World"
print(ss.upper()) # prints HELLO, WORLD

tt = ss.lower()
print(tt) # prints hello, world
print(ss) # prints Hello, world


ss = "    Hello, World    "

els = ss.count("l")
print(els)

print("***"+ss.strip()+"***")

news = ss.replace("o", "***")
print(news)
```

String format:

```python
person = "Samar"
score = 20
print('Hello {}. Your score is {}.".format(name, score))
print('Hello {nm}. Your score is {s1}.".format(s1=score, nm=name))
print('Hello {0}. Your score is {1}. Bye {0}!".format(name, score))


origPrice = 80.99
discount = 33.30
newPrice = (1 - discount/100)*origPrice
calculation = '${:.2f} discounted by {}% is ${:.2f}.'.format(origPrice, discount, newPrice)

```

# Files:

Open/close file:

```python
fileRef = open('school_prompt2.txt','r')
fileRef.close()
```

| Method Name | Use |  Explanation|
|:-----------:|:---:|:-----------:|
| write | filevar.write(astring) | Add a string to the end of the file. filevar must refer to a file that has been opened for writing.|
read(n)|filevar.read()|Read and return a string of n characters, or the entire file as a single string if n is not provided.|
|readline(n)|filevar.readline()| Read and return the next line of the file with all text up to and including the newline character. If n is provided as a parameter, then only n characters will be returned if the line is longer than n. Note the parameter n is not supported in the browser version of Python, and in fact is rarely used in practice, you can safely ignore it.|
|readlines(n)| filevar.readlines()| Returns a list of strings, each representing a single line of the file. If n is not provided then all lines of the file are returned. If n is provided then n characters are read but n is rounded up so that an entire line is returned. Note Like readline readlines ignores the parameter n in the browser.

File iteration: 


```python
f = open("file.txt", "r")

# iterating over characters
for ch in f.read():
    ...

# iterating over lines
for li in f.readlines():
    ...
   
# iterating over lines using the file ref (prefered)
for li in f:
    ...

f.close()
```

Writing a files:

```python
f = open("file.txt", "w") # equivalents to `with open("file.txt", "w") as f`

for number in range(1, 13):
    square = number * number
    f.write(str(square) + "\n") # Note-1: we have to add the \n explicitly, Note-2: We also need to pass a String in contrast to the print

f.close()
```

With keyword:
It is the same for reading (`open` with `r` option) and writing (following example):

```python

# These are the same
f = open("file.txt", "w")
...
f.close()

with open("file.txt", "w") as f:
    ...
```

Dictionaries:

```python
emptyDic = {}
pets = {"cat":12, "dog":6, "elephant":23}

print(pets["dog"]) # prints 6

pets["mouse"] = 3

print(pets["mouse"]) # prints 3

del pets["elephant"] # removes elephant

print(len(pets)) # prints 3
```

Some useful methods:

| Method | Parameters | Description |
|:-------|:-----------|:------------|
| keys   | none       | Returns a view of the keys in the dictionary |
| values | none       | Returns a view of the values in the dictionary |
| items  | none       | Returns a view of the key-value pairs in the dictionary |
| get    | key        | Returns the value associated with key; None otherwise |
| get    | key,alt    | Returns the value associated with key; alt otherwise |

```python
inventory = {'apples': 430, 'bananas': 312, 'pears': 217, 'oranges': 525}

for akey in inventory.keys():
    ...
    
for akey in sorted(inventory.keys()):
    ...

# Or simply
for k in inventory:
    ...

# iterate over the values
for v in inventory.values():
    ...

# iterate over both key and values
for k, v in inventory.items():
    ...

# Check existance
if 'bananas' in inventory:
    print(inventory['bananas'])

# Get the value safely inventory['cherries'] throws an error cause the cherries key doesn't exist in the inventory but get returns None
print(inventory.get("apples"))
print(inventory.get("cherries"))

print(inventory.get("cherries",0))
ks = list(inventory.keys()) # Keys doesn't return the keys as a list, we should convert it using the list() conversion function.

```

Functions:

if you don't return anyting from the function, the return value would be `None`.

In the following code, adding results in an error but multipying not.
```python
x = 9

# has error
def adding():
    x+=1
    print(x)

# No error
def multipying():
    global x
    x+=1
    print(x)

adding()
multipying()
```

Tuple boxing/unboxing

```python
julia = ("Julia", "Roberts", 1967, "Duplicity", 2009, "Actress", "Atlanta, Georgia")

# or equivalently (implicit tuple boxing)
julia = "Julia", "Roberts", 1967, "Duplicity", 2009, "Actress", "Atlanta, Georgia"
print(julia[4])

# (implicit tuple unboxing)
name, surname, birth_year, movie, movie_year, profession, birth_place = julia

(a, b, c, d) = (1, 2, 3) # ValueError: need more than 3 values to unpack

# Swapping values
a = 1
b = 2
(a, b) = (b, a)
```

Use tuple boxing/unboxing in for loop

```python
fruits = ['apple', 'pear', 'apricot', 'cherry', 'peach']

# the following three fors output the same result
for n in range(len(fruits)):
    print(n, fruits[n])
    
for item in enumerate(fruits):
    print(item[0], item[1])

for idx, fruit in enumerate(fruits):
    print(idx, fruit)
```


Use tuple boxing/unboxing with functions:

```python

def circleInfo(r):
    """ Return (circumference, area) of a circle of radius r """
    c = 2 * 3.14159 * r
    a = 3.14159 * r * r
    return c, a

circumference, area = circleInfo(10)

def add(x, y):
    return x + y

print(add(3, 4))
z = (5, 4)
print(add(*z)) # this line will cause the values to be unpacked
print(add(z)) # this line causes an error
```

Optional Parameters
Python acts weired with the optional parameters

```python
initial = 7
# Default values are only evaluated when we declare the function.
# If we change the initial value it doesn't have any effect on f function
def f(x, y =3, z=initial):
    print("x, y, z, are: " + str(x) + ", " + str(y) + ", " + str(z))

initial = 10
f(2) # Prints "x, y, z, are: 2, 3, 7" not "x, y, z, are: 2, 3, 10"

def f(a, L=[]):
    L.append(a)
    return L

print(f(1)) # Prints [1]
print(f(2)) # Prints [1, 2]
print(f(3)) # Prints [1, 2, 3]
print(f(4, ["Hello"])) # Prints ['Hello', 4]
print(f(5, ["Hello"])) # Prints ['Hello', 5]

```

Lambda functions:

```python
def f(x):
    return x - 1

print(f) # prints <function f>
print(type(f)) # prints <class 'function'>
print(f(3)) # prints 2

print(lambda x: x-2) # prints <function <lambda>>
print(type(lambda x: x-2)) # prints <class 'function'>
print((lambda x: x-2)(6)) # prints 6
```

Sorting a list

```python
L1 = [1, 7, 4, -2, 3]

# Option one
L1.sort()
print(L1) # prints [-2, 1, 3, 4, 7]

# Options two (prefered)
L2 = sorted(L1)

# Reversed
L3 = sorted(L1, reverse=True ) # L3 is [7, 4, 3, 1, -2]

# With key

def absolute(x):
    if x >= 0:
        return x
    else:
        return -x

L4 = sorted(L1, key=absolute) # L4 is [1, -2, 3, 4, 7]

```
