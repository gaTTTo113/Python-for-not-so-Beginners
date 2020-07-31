# Lists and other collections

In Python `lists` are written with square brackets:
```
names = ['John', 'Bob', 'Mosh', 'Sarah']
print(names)
print(names[2])
```
>['John', 'Bob', 'Mosh', 'Sarah']
>Mosh

`Lists` can contain different types of objects, also you can have as many layers in list as you want:  
```
matrix = [
	[1, 2, 3],
	[6, 5, 4],
	['Bob', 100500, [7, 8, 9]]
	]
print(matrix[0][2])
print(matrix[2])
print(matrix[2][2][2])
```
>3
>['Bob', 100500, [7, 8, 9]]
>9
 
To add object to end of `list` use `append()`:
```
matrix[0].append(4)
print(matrix)
```
>[[1, 2, 3, 4], [6, 5, 4], ['Bob', 100500, [7, 8, 9]]]

To specify place where new item should be placed use `insert()` :
```
my_list = [1, 2, 3]  
my_list.insert(1, 4)  
print(my_list)
```
>[1, 4, 2, 3]

`clear()` function used to clear list :)
```
matrix[0].clear()
print(matrix)
```
> [ ]

To find index of item use `index()` function:  
```
names = ["Jon", "Ben", "Ron"]
print(names.index(“Ben”))
```
> 1

`copy()`, `sort()` and `reverse()` functions can be really useful:
```
my_list = [1, 3, 4, 2]
my_list.sort()
print(my_list)
```
>[1, 2, 3, 4]
```
my_list.reverse()
print(my_list)
```
>[4, 3, 2, 1]

`copy()` doesn't copy a link to list, but an object itself: 
```
copy_of_my_list = my_list.copy()
my_list.clear()
print(my_list)
print(copy_of_my_list)
```
> [ ]
> [4, 3, 2, 1]

We can “unpack” `list` to several variables:
```
coordinates = [3, 5]
x, y = coordinates
print(f'({x}, {y})')
```
>( 3, 5 )

`Tuples` are list that **can't be modified**, but still can be “unpacked”:
```
numbers = (1, 2, 3)
x, y, z = numbers
```
 
`Dictionary` often used to convert some values:
```
digits_mapper = {
	'1': 'One',
	'2': 'Two',
	'3': 'Three'
	}
number = 12332
output = ''
for digit in str(number):
	output += digits_mapper.get(digit) + ' '
print(output)
```
>One Two Three Three Two 
