# Python-notes


In python result of the / is float !!!!!!!!!!!!!!

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
