# Classes

Create a `class` named *MyClass*, with a property named *x*:
```
class MyClass:
	x = 5
```

Now we can use the `class` named *MyClass* to create `objects`.
Create an `object` named *p1*, and print the value of *x*:
```
p1 = MyClass()
print(p1.x)
```

The examples above are `classes` and `objects` in their simplest form.
All classes have a method called `__init__()`, which is always executed when the class is being initiated, understand it like **class constructor**. Classes can also contain `methods`. Methods in objects are **functions that belong to the object**. We use **1 blank** line to separate them. All methods have default parameter `self`, which represents reference to the current instance of class. It does not have to be named self , you can call it whatever you like, but it has to be **the first parameter** of any function in the class:
```
class Person:
	def __init__(self, name, age):
		self.name = name
		self.age = age
	
	def greet(this_person):
	print(“Hello, my name is “ 
			+ this_person.name)
 

p1 = Person("John", 36)
p1.greet()
print(p1.age)
```
> Hello, my name is John
> 36

**Inheritance** in python.

Any class can be a parent class, to create a class that inherits the functionality from another class, **send the parent class as a `parameter` when creating the child class.**
Also you can use `pass` keyword to create empty class and to avoid error
```
class Student(Person):
	pass


s1 = Student(“Bob”, 21)
s1.greet()
```
> Hello, my name is Bob  

*Note:* The child's `__init__()` function **overrides** the inheritance of the parent's `__init__()` function, to keep the inheritance of the parent's `__init__()` function, **add a call** to the parent's `__init__()` function:
```
class Student(Person):
	def __init__(self, name, age):
		Person.__init__(self, name, age)
```
Python also has a `super()` function that will automatically **inherit all of the methods and properties** from its parent.
```
class Student(Person):
	def __init__(self, name, age):
		super().__init__(name, age)

	def enter_a_classroom(self):
		print(“Good morning!”)

s1 = Student("Bob", 21)
s1.greet()
s1.enter_a_classroom()
```
> Hello, my name is Bob \
> Good morning!
