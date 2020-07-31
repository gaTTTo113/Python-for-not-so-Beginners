
# Loops

  

Using indentations as in `if` statement, let’s do our **simplest `while` loop:**
```
i = 1
while i <= 5:
	print(i)
	i += 1
```

Implementation of guess-game demonstrates `while-else` construction and `break` word:

```
guess_count = 0
guess_limit = 3
secret_number = 5
while guess_count < guess_limit:
	guess = int(input("Guess: "))
	guess_count += 1
	if guess == secret_number:
		print('You won!')
		break
else:
	print('You failed!')
```
 
**Simplest `for` loop:**

```
for letter in 'Python':
	print(letter)
```
  

Also can be used with lists (next article about them):  
```
for item in [“Car”, “Book”, “Phone”]:
	print(item)
```
>Car
>Book
>Phone

`range()` function is powerful tool, returns a sequence of numbers, starting from 0 by default, and increments by 1 (by default), and stops before a specified number:
```
for number in range(10):
	print(number)
```
>0123456789
```
for number in range(5, 10):
	print(number)
```
>56789
```
for number in range(5, 10, 2):
	print(number)
```
>579

`for in for` construction is made by indentations as always:
```
for x in range(2):
	for y in range(2):
		print(f'({x}, {y})')
```
>(0, 0)
(0, 1)
(1, 0)
(1, 1)
```
numbers = [1, 4, 3, 2]
for number in numbers:
	result = ''
	for letter in range(number):
		result += 'x'
	print(result)
```
>x
xxxx
xxx
xx
