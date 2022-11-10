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
```

Use """ to split string in multiple lines.

```python
print("""This message will span
several lines
of the text.""")


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
for _ in range(3):
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


