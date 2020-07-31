
# Python Conditions and If statements

Python supports the usual logical conditions from mathematics:

- Equals: `a == b`
- Not Equals: `a != b`
- Less than: `a < b`
- Less than or equal to: `a <= b`
- Greater than: `a > b`
- Greater than or equal to: `a >= b`

Other programming languages often use curly-brackets to define scope in the code, Python relies on indentation for this purpose.

### If statement:
```
its_raining = True
if its_raining:
	print("It\'s raining!")
else:
	print("It\'s not raining!")
```
If you have only one statement to execute, you can put it on the same line as the if statement:
```
if a > b: print("a is greater than b")
```
**One line** `if else` statement:
```
a = 2
b = 330
print("A") if a > b else print("B")
```
### `else if` construction simplified to `elif`:
```
temperature = 30
if temperature >= 30:
	is_hot = True
	is_cold = False
elif temperature >= 15:
	is_hot = False
	is_cold = False
else:
	is_hot = False
	is_cold = True
```
### `not`, `or`, `and` operands:
```
if is_hot and not is_cold:
	print('hot')
elif is_cold and not is_hot:
	print('cold')
elif is_hot and is_cold:
	print('but how?')
else:
	print('lovely')
```
