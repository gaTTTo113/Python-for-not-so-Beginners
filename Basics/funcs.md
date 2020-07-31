# Functions

  

There are three types of `functions` in Python:

- Built-in functions, such as `help()` to ask for help, `min()` to get the minimum value, `print()` to print an object to the terminal

- User-Defined Functions, which are functions that users create to help them out;

- Anonymous functions, which are also called `lambda` functions because they are not declared with the standard def keyword.

We use **2 blank lines** before and after a function to separate it. Simplest Python `user-defined function`:
```
def greet_user():
	print('Hello!')
greet_user()
```
> Hello!

For using `parameters` simply put them in to the braces:
```
greet_user(user_name):
	print(f’Hello {user_name}!’)


greet_user(‘Kulo’)
```
> Hello Kulo!
  
The following example shows how to use a default parameter value, also named as `keyword argument`:
```
greet_user(user_name=”Bob”):
	print(f’Hello {user_name}!’)


greet_user()
greet_user(“Kulo”)
```
> Hello Bob!
> Hello Kulo!

If you do not know how many arguments would be passed into your function, add a `*` before the parameter name in the function definition.

This way the function will receive a `tuple` of arguments, and can access the items accordingly:
```
def greet_user(*user_names):
	print("Hello "+ str(user_names))


greet_user("Kulo", "Ron", "Bob")
```
> Hello Kulo Ron Bob


If you do not know how many `keyword arguments` would be passed into your function, add two asterisk `**` before the parameter name in the function definition.

This way the function will receive a `dictionary` of arguments, and can access the items accordingly:
```
def greet_user(**user_name):
	print("Hello Mr./Mrs. " 
		+ user_name["last_name"])


greet_user(first_name=”Bob”,
		last_name=”Smith”)
```
 > Hello Mr./Mrs. Smith

Of course we have `return` statement in Python functions:
```
add_values(x, y):
	return x + y


print(add_values(2, 2))
```
> 4

 
Function definitions cannot be empty, but if you for some reason have a function with no content, put in the `pass` statement to avoid getting an error.
```
def my_function():
	pass
```
 
The power of `lambda` is better shown when you use them as an anonymous function inside another function:
```
def my_multiplier(x):
	return lambda y : x * y


my_doubler = my_multiplier(2)
print(my_doubler(11))
```
> 22

