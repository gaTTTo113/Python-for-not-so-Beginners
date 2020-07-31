# Exception Handling

***When an error occurs Python will normally stop and generate an error message.***

These `exceptions` can be handled using the `try` statement:
```
try:
	print(x)
except:
	print("An exception occurred")
```
 
You can define as many `exception blocks` as you want:
```
try:
	print(x)
except NameError:
	print("Variable x is not defined")
except:
	print("Something else went wrong")
```
 
You can use the `else` keyword to define a block of code to be executed if *no errors were raised*:
```
try:
	print("Hello")
except:
	print("Something went wrong")
else:
	print("Nothing went wrong")
```
  
The `finally` block, if specified, will be executed regardless if the `try` block raises an error or not.
Also take a look at nice pattern of writing to the `file` in Python:
```
try:
	f = open("demofile.txt")
	f.write("Lorum Ipsum")
except:
	print("Something went wrong
		 when writing to the file")
finally:
	f.close()
```
  
The `raise` keyword is used to raise an exception.
You can define what kind of error to raise, and the text to print to the user:
```
x = "hello"
if not type(x) is int:
	raise TypeError("Only integers
					 are allowed")
```
