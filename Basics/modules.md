# Modules


Consider a `module` to be the same as a code library.
A file containing a set of `functions` and `variables` you want to include in your application.

This code contains in a file named *my_module* and in `.py` format.
```
def greeting(name):
	print("Hello, " + name)
```
Now we can use the `module` *my_module*, by using the `import` statement and call the greeting function:
```
import my_module

my_module.greeting("Jonathan")
```
  
The `module` can contain `functions`, as already described, but also `variables` of all types (arrays, dictionaries, objects etc):
`my_module.py:`
```
def greeting(name):
	print("Hello, " + name)


members = [“Bob”, “Kulo”, “Ben”]
```
```
import my_module

my_module.greeting(mymodule.members[1])
```
> Hello Kulo
  
You can create an `alias` when you import a module, by using the `as` keyword:
```
import my_module as mm
```
You can choose to import only parts from a module, by using the `from` keyword:
```
from my_module import members
```
There are several **built-in modules** in Python, which you can import and use your your needs.
*For example:* `random`, the *randomize* implementation in Python:
```
import random

for i in range(len(names)):
	print(random.random())
	#random value from 0.0 to 1.0

print(random.randint(-20, 10))
# random int value from -20 to 10

names = ['John', 'Mosh', 'Ben']
print(random.choice(names))
# randomly chosen name from list
```
