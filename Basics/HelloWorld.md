# Hello World, Variables, Strings, Math operations

  

### Let’s start with traditional Hello word app:

  

```
print("Hello Python!")
```

>Hello Python!

  

Python is dynamically typed and garbage-collected, variable names are case-sensitive.

There are also names reserved by Python itself and have a special meaning, to see them all type help(‘keywords’).

### Variable assignment looks like that:

  
```
my_variable = 1
rating = 4.8
name = “Ron”
is_published = False
```
  

Variable reassignment:
```
price = 10
print(price)
```
> 10
```
price = 200
print(price)
```
> 200



  

### Math operators:

```
print(10 + 3)
```
> 13
```
print(10 - 3)
```
> 7
```
print(10 / 3)
```
> 3.3333333333333335
```
print(10 // 3)
```
> 3
```
print(10 % 3)
```
> 1
```
print(10 * 3)
```
> 30
```
print(10 ** 3)
```
> 1000

  

Quick reassignment works with all math operators:

```
x = 3

x += 3

print(x)
```
> 6
```
x = 3
x **= 3
print(x)
```
> 27

Some build-in math functions: 
```
x = -2.9
print(round(x))
print(abs(x))
```
> -3
> 2.9
  
[*more here*](https://www.linuxtopia.org/online_books/programming_books/python_programming/python_ch04s04.html)

### Math module:
Python has a built-in module that you can use for mathematical tasks.

The  `math`  module has a set of methods and constants.

first import module on the top of your python file:
```
import math
```
next you can use it by calling `math.name_of_function`:
```
x = 4.4
print(math.ceil(x))
print(math.floor(x))
print(math.cos(0))
```
> 5
> 4
> 1.0

### Strings
Strings are Python’s super-power :)
To assign string use ‘’ or “”:
```
my_string = 'like that'
my_string = "or like that"
```
The choice between both the types (single quotes and double quotes) depends on the programmer’s choice. Generally, double quotes are used for string representation and single quotes are used for regular expressions, dict keys or SQL.
```
my_message = “here is my string”
my_key = ‘jks5d22ks&1a’
```
  

If you need to use special characters in your string, mark them with ‘  **\\**  ’:
```
item = “Ron\’s pizza”
```
Also Python offers **string slicing**:

```
numbers = “0123456789”
print(numbers)
```
> 0123456789
```
print(numbers[0])
```
> 0
```
print(numbers[-1])
```
> 9
```
print(numbers[0:3])
```
> 012
```
print(numbers[:3])
```
> 012
```
print(numbers[3:])
```
> 3456789
```
print(numbers[1:-1])
```
> 12345678
```
print(numbers[:])
```
> 0123456789

**Formatted Strings** and useful functions:

```
first = "Ron”
last = “Smith”
msg = f'{first} {last} is a coder'
print(msg)
```
> Ron Smith is a coder
```
print(msg.upper())
```
> RON SMITH IS A CODER
```
print(msg.lower())
```
> ron smith is a coder
```
print(msg.find('S'))
```
> 4
```
print(msg.replace(f'{first}', 'Name'))
```
> Name Smith is a coder
```
print("some another string" in msg)
```
> False
```
print(first in msg)
```
> True
 
```
some_info_for_you = '''that's -->
how you can store
complicated strings
-''- /?|
easily
'''
print(some_info_for_you)
```
> that's --> \
> how you can store \
> complicated strings \
> -''- /?| \
> easily 

### input() function 
Takes users input to string:
```
answer = input("What you want to input?")
print("Here it is: " + answer)
```
 

To convert input use this functions:
int() float() double() bool() str()

```
birth_year = input('Put your birth year: ')
print("Most likely you are "
	+ str(2020 - int(birth_year))
	+ " years old")
```
